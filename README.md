# found-with-claude

An autonomous loop for founders building from idea to Demo Day.

---

Most AI coding tools start at code. Founders don't.

Founders start with uncertainty — is this problem real? Who has it? What should
we build first? What are the signals that tell us it's working?

`found-with-claude` is a Claude Skills pack that covers the whole loop.
Run `/loop` and it drives autonomously — synthesizing, analyzing, deciding —
stopping only when it needs something only a founder can do: go talk to
customers, build the prototype, do the outreach, run the experiments.

Drop the result. Run `/loop` again. It picks up where it left off.

---

## How it works

```
/new-startup        ← sets up your workspace, captures initial context
/loop               ← runs until it needs you, then stops with exact instructions
                       drop the requested input, run /loop again to resume
```

The loop knows four natural pause points — where AI can't substitute for the founder:

| Block | What the loop needs | What you do |
|-------|--------------------|----|
| Discovery | Customer interview transcripts | Talk to 5–10 people, drop notes |
| Build | Prototype + user reactions | Build in prototype-with-claude, drop build-notes.md |
| Outreach execution | Who responded and what they said | Do the outreach, drop outreach-results.md |
| Experiment execution | What the experiments showed | Run the experiments, drop experiment-results.md |

Everything else — opportunity mapping, synthesis, customer simulation, product
strategy, prototype scoping, PMF analysis, growth backlog, fundraising narrative,
Demo Day script — runs autonomously.

---

## The skills

15 skills total. `/loop` orchestrates them. You can also invoke any skill directly.

```
.claude/skills/
├── new-startup/                 → /new-startup
├── loop/                        → /loop
├── founder-opportunity-map/     → /founder-opportunity-map
├── customer-discovery-synthesizer/ → /customer-discovery-synthesizer
├── synthetic-customer-panel/    → /synthetic-customer-panel
├── product-strategy-brief/      → /product-strategy-brief
├── prototype-scope/             → /prototype-scope
├── prototype-review/            → /prototype-review
├── first-users-outreach/        → /first-users-outreach
├── pmf-signal-review/           → /pmf-signal-review
├── growth-experiment-backlog/   → /growth-experiment-backlog
├── founder-hiring-scorecard/    → /founder-hiring-scorecard
├── fundraising-narrative/       → /fundraising-narrative
├── demo-day-script/             → /demo-day-script
└── weekly-founder-review/       → /weekly-founder-review
```

---

## Why this exists

Most "AI for founders" tooling treats founders as developers and stops at software
prototyping. But prototyping is step 5 of an 11-step journey.

Before you write a line of code, you need to:
- Find a problem that is genuinely painful
- Talk to people who have it
- Understand what they are already doing about it
- Decide what to build and why
- Define what success looks like

After you ship, you need to:
- Get the first 10 users
- Read the signals they send
- Know when you have PMF and when you do not
- Hire the right first person
- Tell the story to investors

Claude can compress every phase of this loop — not just the coding phase.

---

## The founder learning loop

```
Problem → Customers → Synthesis → Strategy → Prototype → Users → PMF → Growth → Hire → Raise → Demo Day
   ↑                                                                                               ↓
   └───────────────────────────── What did we learn? ─────────────────────────────────────────────┘
```

`/loop` runs this. The skills are the mechanism. The loop state file tracks where
you are. When the loop needs the founder, it says exactly what, where, and how much.

---

## Skill map

| Phase | Question | Skill |
|-------|----------|-------|
| Setup | — | `/new-startup` |
| **Orchestration** | **What should run next?** | **`/loop`** |
| Find a problem | Is this pain real and underserved? | `/founder-opportunity-map` |
| Customer discovery | Who has it and what do they say? | `/customer-discovery-synthesizer` |
| Customer simulation | What would real users say about this idea? | `/synthetic-customer-panel` |
| Product strategy | What do we build and why? | `/product-strategy-brief` |
| Prototype planning | What exactly are we building? | `/prototype-scope` |
| Prototype review | Does the prototype prove the thesis? | `/prototype-review` |
| First users | Who are they and how do we reach them? | `/first-users-outreach` |
| PMF sprint | Are we seeing the signals that matter? | `/pmf-signal-review` |
| Growth | What lever do we pull next? | `/growth-experiment-backlog` |
| Hiring | Who is the right first hire? | `/founder-hiring-scorecard` |
| Fundraising | What is the story investors need to hear? | `/fundraising-narrative` |
| Demo Day | Can we land this in 2 minutes on stage? | `/demo-day-script` |
| Weekly | What did we learn? | `/weekly-founder-review` |

---

## Quickstart

```bash
# 1. Clone
git clone https://github.com/sinned/found-with-claude
cd found-with-claude

# 2. Open Claude Code
claude

# 3. Set up your startup workspace
/new-startup

# 4. Let the loop run
/loop
# → runs autonomously until it needs you
# → tells you exactly what to do when it stops
# → drop the input, run /loop again to resume
```

No setup. No API keys. No boilerplate.

---

## How the loop stops

When `/loop` hits a phase it can't run without you, it outputs a block report:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⏸  LOOP PAUSED — founder input needed

Phase completed in this run:
  ✅ opportunity-map
  ✅ (awaiting your interviews)

Paused at: discovery

What the loop needs:
  Customer interview transcripts — raw notes are fine

Where to put them:
  work/startup-1/customer-discovery-synthesizer/customer-transcript-N.md

What "enough" looks like:
  At least 3 files (more = better synthesis)

To resume:
  1. Do 5–10 customer calls
  2. Drop your notes at the path above
  3. Run /loop
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

The loop state is saved in `work/[startup]/loop-state.md` between runs.

---

## Work is organized by startup

Each startup gets its own workspace:

```
work/
  .current            ← active startup name (e.g., "startup-1")
  startup-1/
    loop-state.md     ← where the loop is, what it's waiting for
    founder-opportunity-map/
    customer-discovery-synthesizer/
    ...all 13 skill folders
  startup-2/
    ...
```

Run `/new-startup` to create a new one. `work/.current` tracks which is active.
All skills and `/loop` read `work/.current` automatically.

---

## Where gstack fits

[gstack](https://github.com/garrytan/gstack) is a global Claude Code skills pack
for the engineering sprint: plan, build, review, QA, ship.

**The handoff:** `/prototype-scope` (here) defines what to build. gstack's
`/office-hours` and `/autoplan` plan it. `/review`, `/qa`, `/ship` ship it.
`/prototype-review` (here) evaluates the result. `/loop` orchestrates all of it.

See `docs/gstack-integration.md` for details.

---

## Where `prototype-with-claude` fits

The sibling repo [`prototype-with-claude`](https://github.com/sinned/prototype-with-claude)
is the dedicated build environment for the prototyping step.

**How it connects:**
1. `/prototype-scope` (here) → defines what to build
2. Open `https://github.com/sinned/prototype-with-claude` → build and eval the AI behavior
3. Drop `build-notes.md` in `work/[startup]/prototype-review/`
4. Run `/loop` → resumes with `/prototype-review` automatically

---

## For Anthropic reviewers

Where to look:
- `CLAUDE.md` — project instructions for Claude Code (includes path resolution logic)
- `.claude/skills/loop/SKILL.md` — the autonomous orchestrator
- `.claude/skills/` — all 15 skills
- `work/startup-1/loop-state.md` — example loop state
- `work/startup-1/customer-discovery-synthesizer/` — 10 sample interview transcripts
- `docs/founder-journey-map.md` — how the skills connect

What to run:
```
/new-startup
/loop
```

What makes this different:
- `/loop` runs the full journey autonomously, not just individual skills
- Stops at the four phases where AI can't substitute for founder work
- Loop state persists between runs so it resumes exactly where it left off
- Each startup gets its own workspace; multiple startups can coexist

---

## The broader "Claude for…" pattern

- `prototype-with-claude` → Claude for AI feature prototyping
- `found-with-claude` → Claude for company building, idea to Demo Day
- (future) `investing-with-claude` → Claude for sourcing, diligence, portfolio ops

Each is a self-contained Claude Skills pack for a professional context — turning
Claude Code from a coding assistant into a workflow accelerator for the whole job.
