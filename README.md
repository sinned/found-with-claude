# found-with-claude

A Claude Skills pack for founders building from idea to Demo Day.

---

Most AI coding demos start with code. Founders do not.

Founders start with uncertainty:
- Is this problem painful?
- Who has it?
- What are they doing today?
- What should we build first?
- What is the riskiest assumption?
- How do we get the first users?
- What signals tell us we are onto something?

This repo gives founders reusable Claude Skills for that entire journey.

---

## What this is

A collection of 13 opinionated Claude Skills covering the full company-building loop.
Clone it, open it in Claude Code, and invoke the skills directly. Each skill is a
structured workflow — not a chatbot conversation, but a repeatable founder process.

```
.claude/skills/
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
prototyping. But prototyping is week 5 of a 12-week journey.

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

Each phase has an urgent question. Each question has a skill. The skills are designed
to be fast: 10 minutes of input, structured output you can act on the same day.

---

## Skill map

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
| Weekly | What did we learn this week? | `/weekly-founder-review` |

---

## Quickstart

```bash
# 1. Clone
git clone https://github.com/sinned/found-with-claude
cd found-with-claude

# 2. Open Claude Code
claude

# 3. Drop your raw context
# Put your notes, transcripts, or ideas in examples/founder-context.md

# 4. Start at the beginning
/founder-opportunity-map

# Or jump to wherever you are in the journey
/customer-discovery-synthesizer
/product-strategy-brief
/weekly-founder-review
```

No setup. No API keys. No boilerplate. Just open Claude Code and invoke a skill.

---

## How to use the skills

### Input: bring your raw material

Every skill is designed to work from rough input. Drop your actual notes, transcripts,
and data into `examples/`. You do not need to clean it up first.

- `examples/founder-context.md` — who you are, what you are building, what you know
- `examples/messy-founder-notes.md` — raw notes from calls, walks, observations
- `examples/customer-transcript-1.md` — interview transcripts verbatim
- Anything else you have: screenshots descriptions, competitor notes, user emails

### Invocation: just run the command

```
/customer-discovery-synthesizer
```

Claude will find your transcripts, synthesize them, and produce structured output.
The skill tells Claude exactly what to look for and what to produce.

### Output: structured documents you can act on

Each skill produces a specific artifact: a memo, a brief, a scorecard, a script.
Outputs are saved in the repo so you can reference them across skills.

### Iteration: run skills multiple times

Run `/founder-opportunity-map` before talking to customers. Run it again after.
The second output is almost always different. That difference is what you learned.

---

## The idea-to-Demo-Day journey

See `journeys/` for week-by-week worked examples. The full arc:

| Week | Focus | Primary skill |
|------|-------|---------------|
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
| 12 | Post-Demo Day | `/weekly-founder-review` |
| Every week | Review | `/weekly-founder-review` |

---

## Where gstack fits

[gstack](https://github.com/garrytan/gstack) (by Garry Tan, YC President & CEO) is a
global Claude Code skills pack for the engineering sprint: plan, build, review, QA,
ship. It installs once to `~/.claude/skills/gstack/` and works in any repo.

**The handoff:** `/prototype-scope` (here) defines what to build. gstack's `/office-hours`
and `/autoplan` plan it. `/review`, `/qa`, `/ship` build and ship it. `/prototype-review`
(here) evaluates the result.

gstack and `found-with-claude` are complementary — gstack lives inside the build
sprint, this repo covers everything around it.

See `docs/gstack-integration.md` for the full integration guide, including how to
pass context from `/prototype-scope` into gstack's `/office-hours`, how to combine
the weekly `/retro` and `/weekly-founder-review`, and when to use gstack vs.
`prototype-with-claude` for prototyping AI features.

---

## Where `prototype-with-claude` fits

This repo covers the full founder journey. The sibling repo `../prototype-with-claude`
is the dedicated build environment for Week 5 — the prototyping sprint itself.

**What `prototype-with-claude` does:**
- Teaches the Write SKILL.md → eval → improve → export to production Python workflow
- Provides built-in skills: `/qualify-lead`, `/research-agent`, `/generate-content`
- Shows how to graduate a working Claude behavior to production via the Agent SDK
- Demonstrates the three skill patterns: Research & Synthesize, Score & Classify, Generate & Iterate

**How it connects to this repo:**
1. `/prototype-scope` (here) → defines what to build
2. Open `../prototype-with-claude` → build it using Claude Skills
3. `/prototype-review` (here) → evaluate the result against the original strategy

The prototyping sprint is where you build the AI behavior your product depends on.
`prototype-with-claude` is how you do that without writing SDK code before the
behavior is validated.

See `docs/prototype-with-claude-integration.md` for the full integration context.

---

## Example workflow

You are a founder who suspects there is a pain around how early-stage startups
manage their investor updates.

**Week 1 — Map the opportunity:**
```
/founder-opportunity-map
```
Output: ranked opportunity memo. Investor updates rank #2. Your #1 surprise: the
real pain is not writing the update — it is synthesizing what actually happened.

**Week 2 — Talk to founders:**
You do 7 calls. Drop the transcripts in `examples/`. Run:
```
/customer-discovery-synthesizer
```
Output: synthesis across 7 interviews. Clear pattern: founders spend 3-4 hours
pulling together data that lives in 6 different tools before they can write a word.

**Week 3 — Stress-test the concept:**
```
/synthetic-customer-panel
```
Output: 5 founder archetypes react to your proposed concept. Two archetypes say
they would use it. Three say they already have a workaround.

**Week 4 — Write the strategy:**
```
/product-strategy-brief
```
Output: one-page brief. Target: seed-stage founders with 10-20 investors. Core bet:
auto-pull data from Stripe, Linear, and bank accounts. The brief reveals your
riskiest assumption: founders trust AI-generated numbers in investor-facing docs.

**Week 5 — Build:**
```
/prototype-scope
```
Output: scope document. One week. One job. Open `../prototype-with-claude`. Build it.

**Week 6 — Get users:**
```
/first-users-outreach
```
Output: outreach sequence targeting founders in your network. First 10 users found
in 5 days.

---

## For Anthropic reviewers

This repo is the `found-with-claude` companion to `prototype-with-claude`.

Where to look:
- `CLAUDE.md` — project-level instructions for Claude Code
- `.claude/skills/` — the 13 founder skills (these are the primary artifact)
- `docs/founder-journey-map.md` — how the skills connect
- `docs/prototype-with-claude-integration.md` — integration with the sibling repo
- `journeys/week-01-find-a-problem.md` — worked example of the first week
- `examples/` — sample founder inputs and skill outputs

What makes this different:
- Skills cover the full company-building loop, not just the coding phase
- Each skill is opinionated and structured, not open-ended
- The skills are designed to work from rough founder input
- The weekly review is a meta-skill that ties everything together

What to run:
```
/founder-opportunity-map
/customer-discovery-synthesizer
/weekly-founder-review
```

---

## Why this is more than DevRel

The standard "AI for founders" narrative: use AI to write code faster.

The problem with that narrative: most founding failures are not caused by slow coding.
They are caused by building the wrong thing, talking to the wrong customers, writing
the wrong pitch, or hiring the wrong person.

Claude is not just a code accelerator. It is a thinking partner for the full
founder job. The skills in this repo are designed to compress the learning loop,
not the coding loop.

When a founder runs `/customer-discovery-synthesizer` after 7 customer calls, they
get a structured synthesis in minutes instead of days. When they run
`/synthetic-customer-panel`, they find out which objections they have not answered
before they build anything. When they run `/weekly-founder-review`, they leave
Friday with a clear decision about what matters most next week.

This is what "Claude for founders" actually means: compress every phase of the
company-building loop, not just the prototyping phase.

---

## The broader "Claude for…" idea

`found-with-claude` is one instance of a pattern:

- `prototype-with-claude` → Claude for AI feature prototyping
- `found-with-claude` → Claude for company building
- (future) `investing-with-claude` → Claude for sourcing, diligence, and portfolio ops
- (future) `research-with-claude` → Claude for academic research workflows

Each repo is a self-contained Claude Skills pack for a specific professional context.
Each one turns Claude Code from a coding assistant into a workflow accelerator for
the entire job — not just the parts that involve writing code.

The pattern works because Claude Code skills are just plain-text job descriptions.
Any workflow that can be described clearly can be a skill.
