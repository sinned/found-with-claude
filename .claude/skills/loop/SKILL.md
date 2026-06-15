---
name: loop
description: Autonomous founder loop. Runs all skills it can, stops when it needs the founder, and saves exactly what's needed to resume. Run /loop to advance, resume after blocking, or check current state.
---

# The Founder Loop

Runs the founding journey autonomously — skill by skill — stopping only when it
needs real-world input from the founder. Saves the exact block condition so the
founder knows what to do and the loop knows when to resume.

## How to use

- **Start:** `/loop` — reads current state and runs what it can
- **Resume after doing real-world work:** drop input files, then `/loop` again
- **Check where you are:** `/loop` with no context will report current state

## Before running

1. Read `work/.current` to get the active startup (e.g., `startup-1`)
2. Set `STARTUP = work/[startup]` — use this prefix for all paths below
3. Read `STARTUP/ops/loop-state.md` if it exists. If not, this is the first run — create it.

---

## The phase table

Work through phases in order. For each phase:
- Check if already DONE (output file exists) → skip, mark done, move on
- Check if RUNNABLE (input files exist, output doesn't) → run the skill
- Check if BLOCKED (inputs don't exist) → write block, stop

| # | Phase | Autonomous? | Input exists when... | Output file |
|---|-------|-------------|----------------------|-------------|
| 0 | `onboarding` | — | `opportunity/founder-context.md` exists | same |
| 1 | `opportunity-map` | ✅ yes | founder-context.md exists | `opportunity/opportunity-memo.md` |
| 2 | `discovery` | ❌ blocked | — | `customers/customer-transcript-1.md` (≥3 files) |
| 3 | `synthesis` | ✅ yes | ≥3 `customer-transcript-*.md` files | `customers/synthesis.md` |
| 4 | `panel` | ✅ yes | `synthesis.md` exists | `customers/simulated-panel.md` |
| 5 | `strategy` | ✅ yes | synthesis + panel outputs exist | `product/strategy-brief.md` |
| 6 | `prototype-scope` | ✅ yes | `strategy-brief.md` exists | `product/prototype-scope.md` |
| 7 | `build` | ❌ blocked | — | `product/build-notes.md` |
| 8 | `prototype-review` | ✅ yes | `build-notes.md` exists | `product/prototype-review.md` |
| 9 | `first-users` | ✅ yes | `prototype-review.md` exists | `traction/outreach-plan.md` |
| 10 | `outreach-execution` | ❌ blocked | — | `traction/outreach-results.md` |
| 11 | `pmf-review` | ✅ yes | `outreach-results.md` exists | `traction/pmf-signals.md` |
| 12 | `growth-experiments` | ✅ yes | `pmf-signals.md` exists | `traction/experiment-backlog.md` |
| 13 | `experiment-execution` | ❌ blocked | — | `traction/experiment-results.md` |
| 14 | `pmf-review-2` | ✅ yes | `experiment-results.md` exists | `traction/pmf-signals-2.md` |
| 15 | `hiring` | ✅ yes* | `strategy-brief.md` exists | `team/hiring-scorecard-[role].md` |
| 16 | `fundraising` | ✅ yes | `pmf-signals.md` exists | `pitch/fundraising-narrative.md` |
| 17 | `demo-day` | ✅ yes | `fundraising-narrative.md` exists | `pitch/demo-day-script.md` |
| ∞ | `weekly-review` | ✅ ongoing | always | `ops/weekly-review-[date].md` |

*Phase 15 (hiring) runs in parallel once the strategy is clear — not gated on PMF.

---

## Step-by-step execution

### Step 1 — Establish current state

Read `STARTUP/ops/loop-state.md`. Extract:
- `status` (RUNNING / BLOCKED / DONE)
- `current_phase` (the phase name from the table)
- `blocked_on` (what the founder needs to provide, if BLOCKED)
- `resolved_when` (the condition that unblocks it)

If `loop-state.md` does not exist, treat as first run: set phase to `onboarding`,
status to RUNNING.

### Step 2 — If BLOCKED, check the resolution condition

Use the `resolved_when` field from loop-state.md to check whether the block
has been cleared.

**Resolution checks by phase:**

- `discovery`: Count files matching `STARTUP/customers/customer-transcript-*.md`.
  Resolved if count ≥ 3.

- `build`: Check whether `STARTUP/product/build-notes.md` exists.
  Resolved if file exists and is non-empty.

- `outreach-execution`: Check whether `STARTUP/traction/outreach-results.md` exists.
  Resolved if file exists and is non-empty.

- `experiment-execution`: Check whether `STARTUP/traction/experiment-results.md` exists.
  Resolved if file exists and is non-empty.

**If still blocked:** Report the current block (see Block Report format below).
Update the `last_checked` field in loop-state.md. Stop.

**If resolved:** Log "Block cleared: [phase]" in loop-state.md history.
Set status to RUNNING. Advance to the next phase. Continue to Step 3.

### Step 3 — Run autonomous phases in sequence

For each phase starting from `current_phase`:

1. **Check if already done:** Does the output file exist? If yes, mark DONE in history,
   advance phase, continue.

2. **Check if runnable:** Do the required inputs exist? If yes, invoke the corresponding
   skill (`/founder-opportunity-map`, `/customer-discovery-synthesizer`, etc.).
   Write the output to the path in the phase table.
   Mark DONE in history. Advance phase. Continue.

3. **Check if blocked:** Inputs don't exist and this is a human-input phase.
   Write the block. Stop.

Run as many autonomous phases in sequence as possible before stopping.
Do not stop between autonomous phases — chain them. The loop should advance
multiple phases in a single run when it can.

### Step 4 — Write block (when stopping)

When the loop hits a blocked phase, write the Block Report to the conversation
AND update `STARTUP/ops/loop-state.md` with the block details.

**Block Report format:**
```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⏸  LOOP PAUSED — founder input needed
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Phase completed in this run:
  ✅ [list each phase that just ran]

Paused at: [phase name]

What the loop needs:
  [Clear 1-2 sentence description of what the founder needs to do]

Where to put it:
  [Exact file path(s)]

What "enough" looks like:
  [The specific condition that will unblock — e.g., "at least 3 transcript files"]

To resume:
  1. [Numbered real-world action steps]
  2. Drop the results at the paths above
  3. Run /loop

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Step 5 — Update loop-state.md

After every run (whether it blocked or completed phases), rewrite
`STARTUP/ops/loop-state.md` with the full current state.

---

## loop-state.md format

```markdown
# Loop State

*Startup: [startup-name]*
*Last run: [ISO datetime]*
*Status: RUNNING | BLOCKED | DONE*
*Current phase: [phase-name]*

## Block (if status = BLOCKED)

**Waiting for:** [what the founder needs to provide]
**Where to put it:** `[exact file path]`
**Resolved when:** [specific condition — file exists, count ≥ N, etc.]
**Last checked:** [ISO datetime]

### Founder action queue
1. [Numbered real-world steps]
2. Drop results at the path above
3. Run `/loop` to resume

## Phase history

| Phase | Status | Date | Notes |
|-------|--------|------|-------|
| onboarding | ✅ done | [date] | founder-context.md exists |
| opportunity-map | ✅ done | [date] | opportunity-memo.md written |
| discovery | ⏸ blocked | [date] | waiting for transcripts |

## What the loop did on last run

[Brief summary — which phases ran, what outputs were produced]

## Loop run log

- [datetime]: [what happened in one line]
- [datetime]: [what happened in one line]
```

---

## Handling the first run (no loop-state.md yet)

If `STARTUP/ops/loop-state.md` does not exist:

1. Check whether `STARTUP/opportunity/founder-context.md` exists.
   - If not: tell the founder to run `/new-startup` first, stop.
   - If yes: treat onboarding as done, set current phase to `opportunity-map`.

2. Scan all phase output files to determine what's already been done
   (the founder may have run individual skills manually before starting the loop).
   Mark those phases as done in the initial history.

3. Create `STARTUP/ops/loop-state.md` with the derived current state.

4. Continue from Step 3.

---

## Edge cases

**Founder has already run some skills manually:** Detect completed phases by
checking output files. Mark them done. Don't re-run them. Pick up from the
first incomplete phase.

**Founder wants to re-run a phase:** They can delete the output file and run
`/loop`. The loop will re-run that phase.

**Founder wants to skip a phase:** They can create the expected output file
with a note like `# Skipped`. The loop will see it as done and move on.

**Hiring (phase 15) runs in parallel:** After `strategy` is complete (phase 5),
if the founder mentions hiring or there's a role to fill, run `/founder-hiring-scorecard`
independently of the main phase sequence. Don't let it block the primary loop.

**Weekly review runs always:** At the end of every loop run (blocked or not),
check if today is Friday or if it has been ≥6 days since the last weekly review.
If so, run `/weekly-founder-review` before stopping.
