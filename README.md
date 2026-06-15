# found-with-claude

A Claude Skills pack for founders building from idea to Demo Day.

---

Most AI coding tools start at code. Founders don't.

Founders start with uncertainty — is this problem real? Who has it? What should
we build first? What signals tell us it's working?

This repo gives founders 13 structured Claude Skills for that entire journey.
Each skill is a repeatable process, not a chatbot conversation. Drop in your raw
material — messy notes, interview transcripts, usage data — and get structured
output you can act on the same day.

---

## The skills

| Phase | Question | Skill |
|-------|----------|-------|
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

# 4. Start at the beginning — or wherever you are
/founder-opportunity-map
```

No setup. No API keys. No boilerplate. Just open Claude Code and invoke a skill.

---

## How to use it

### Input: bring your raw material

Every skill works from rough input. Drop your actual notes, transcripts, and data
into the relevant corpus folder. No cleanup needed.

- `work/[startup]/opportunity/founder-context.md` — who you are, what you know
- `work/[startup]/opportunity/founder-notes.md` — raw observations
- `work/[startup]/customers/customer-transcript-1.md` — interview transcripts

### Output: structured artifacts, not chat

Each skill produces a specific document: a memo, a brief, a scorecard, a script.
Outputs are saved in the relevant corpus folder so they feed directly into the next skill.

### Chain: each output is the next skill's input

```
/founder-opportunity-map   → opportunity memo
/customer-discovery-synthesizer  → synthesis of interviews
/synthetic-customer-panel  → stress-test before building
/product-strategy-brief    → one-page brief
/prototype-scope           → what to build, exactly
/prototype-review          → did it prove the thesis?
/first-users-outreach      → how to find the first 10 users
/pmf-signal-review         → are the signals real?
...
```

### Iterate: run skills multiple times

Run `/founder-opportunity-map` before talking to customers. Run it again after.
The difference between runs is what you learned.

---

## Work is organized by startup

```
work/
  .current          ← active startup (e.g., "startup-1")
  startup-1/
    opportunity/    ← problem space, market analysis, founder context
    customers/      ← interview transcripts, synthesis, simulated panels
    product/        ← strategy brief, prototype scope, build evidence
    traction/       ← outreach, PMF signals, experiments
    team/           ← hiring scorecards
    pitch/          ← fundraising narrative, demo day script
    ops/            ← weekly reviews, loop state
  startup-2/
    ...
```

Organized by knowledge corpus — not by skill. Every skill reads from and writes to
the appropriate folder. Run `/new-startup` to create a workspace. `work/.current` tracks
which is active.

The knowledge store at `knowledge/[startup]/` accumulates structured facts as skills run —
designed for future export to an external durable store.

---

## The idea-to-Demo-Day journey

| Step | Focus | Skill |
|------|-------|-------|
| 1 | Find a problem | `/founder-opportunity-map` |
| 2 | Customer discovery | `/customer-discovery-synthesizer` |
| 3 | Customer simulation | `/synthetic-customer-panel` |
| 4 | Product strategy | `/product-strategy-brief` |
| 5 | Build prototype | `/prototype-scope` → `prototype-with-claude` |
| 6 | First users | `/first-users-outreach` |
| 7 | PMF sprint | `/pmf-signal-review` |
| 8 | Growth | `/growth-experiment-backlog` |
| 9 | Hiring | `/founder-hiring-scorecard` |
| 10 | Fundraising | `/fundraising-narrative` |
| 11 | Demo Day | `/demo-day-script` |
| Ongoing | Review | `/weekly-founder-review` |

---

## Where gstack fits

[gstack](https://github.com/garrytan/gstack) is a global Claude Code skills pack
for the engineering sprint: plan, build, review, QA, ship.

**The handoff:** `/prototype-scope` (here) defines what to build. gstack's
`/office-hours` and `/autoplan` plan it. `/prototype-review` (here) evaluates the result.

See `docs/gstack-integration.md` for details.

---

## Where `prototype-with-claude` fits

The sibling repo [`prototype-with-claude`](https://github.com/sinned/prototype-with-claude)
is the dedicated build environment for the prototyping step.

1. `/prototype-scope` (here) → defines what to build
2. Open `https://github.com/sinned/prototype-with-claude` → build and eval the AI behavior
3. `/prototype-review` (here) → evaluate the result against the original strategy

---

## Once you know the process: `/loop`

After you've run through the journey once and understand how the skills connect,
`/loop` can orchestrate the whole thing autonomously.

It runs every skill it can, and stops with exact instructions when it needs
real-world founder input — customer interviews, the prototype build, outreach,
experiment results. Drop the input, run `/loop` again, it resumes.

```bash
/loop   # runs what it can, stops when it needs you
```

Loop state is saved in `work/[startup]/loop-state.md` between runs.

---

## For Anthropic reviewers

Where to look:
- `CLAUDE.md` — project instructions for Claude Code
- `.claude/skills/` — all 15 skills (13 journey skills + `/new-startup` + `/loop`)
- `work/startup-1/` — demo startup with sample transcripts and outputs
- `docs/founder-journey-map.md` — how the skills connect

What to run:
```
/new-startup
/founder-opportunity-map
/customer-discovery-synthesizer
/weekly-founder-review
```

What makes this different:
- Skills cover the full company-building loop, not just the coding phase
- Each skill is opinionated and structured — specific input, specific output
- Skills chain: each output is the next skill's input
- Work is organized per-startup so multiple ideas can coexist

---

## The broader "Claude for…" pattern

- `prototype-with-claude` → Claude for AI feature prototyping
- `found-with-claude` → Claude for company building, idea to Demo Day
- (future) `investing-with-claude` → Claude for sourcing, diligence, portfolio ops

Each is a self-contained Claude Skills pack for a professional context — turning
Claude Code from a coding assistant into a workflow accelerator for the whole job.
