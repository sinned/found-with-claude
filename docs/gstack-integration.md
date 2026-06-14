# gstack Integration

How `founding-with-claude` and [gstack](https://github.com/garrytan/gstack) work together.

---

## What gstack is

gstack (by Garry Tan, President & CEO of Y Combinator) is a Claude Code skills pack
that turns Claude Code into a virtual engineering team. 23+ skills covering the full
software development sprint:

**Think → Plan → Build → Review → Test → Ship → Reflect**

Key skills:
- `/office-hours` — YC-style product interrogation with six forcing questions
- `/plan-ceo-review` — strategic challenge, scope modes, 10-section review
- `/plan-eng-review` — architecture, data flow, edge cases, test matrix
- `/autoplan` — one command, full CEO → design → eng review pipeline
- `/review` — staff engineer code review, auto-fixes obvious issues
- `/qa` — real Chromium browser, finds bugs, fixes with atomic commits
- `/ship` — sync, test, audit coverage, push, open PR
- `/cso` — OWASP Top 10 + STRIDE threat model
- `/retro` — weekly engineering retrospective

gstack installs globally: `~/.claude/skills/gstack/`. It is not project-specific.
It works in any repo where you do engineering work.

---

## What this repo is

`founding-with-claude` is a project-level skills pack covering the full
**company-building** loop — everything around the build sprint, not inside it:

**Problem → Customers → Strategy → [Build] → Users → PMF → Growth → Demo Day**

The `[Build]` phase is where gstack lives. Everything else is `founding-with-claude`.

---

## How they fit together

The two repos are complementary. They do not overlap on any skill:

| Phase | founding-with-claude | gstack |
|-------|---------------------|--------|
| Find a problem | `/founder-opportunity-map` | — |
| Customer discovery | `/customer-discovery-synthesizer` | — |
| Customer simulation | `/synthetic-customer-panel` | — |
| Product strategy | `/product-strategy-brief` | — |
| **Scope the build** | **`/prototype-scope`** ← handoff → | **`/office-hours`, `/autoplan`** |
| **Plan the build** | — | **`/plan-ceo-review`, `/plan-eng-review`** |
| **Build** | — | **`/review`, `/qa`, `/ship`** |
| **Review the build** | **`/prototype-review`** ← handoff | — |
| First users | `/first-users-outreach` | — |
| PMF signals | `/pmf-signal-review` | — |
| Growth | `/growth-experiment-backlog` | — |
| Security | — | `/cso` |
| Weekly eng retro | — | `/retro` |
| Weekly founder review | `/weekly-founder-review` | — |
| Hiring | `/founder-hiring-scorecard` | — |
| Fundraising | `/fundraising-narrative` | — |
| Demo Day | `/demo-day-script` | — |

---

## The build sprint handoff

The most important integration point is Week 5 of the founder journey:

```
founding-with-claude              gstack (or prototype-with-claude)
────────────────────              ────────────────────────────────
/prototype-scope
 → produces scope doc
   with "the one job"
   and success criteria
          │
          ▼
          └──── open your product repo ────►  /office-hours
                                               (paste the one job from scope doc)
                                               ↓
                                              /autoplan
                                               (CEO + design + eng review)
                                               ↓
                                              implement
                                               ↓
                                              /review  → auto-fix
                                               ↓
                                              /qa  → real browser, fix bugs
                                               ↓
                                              /ship  → PR opened
                                               │
                                               ▼
                                     ◄─── return to founding-with-claude ────
          ┌──────────────────────────────────────────────────────────────────┘
          ▼
/prototype-review
 → evaluate the shipped PR
   against the original scope
   and strategy
```

### Passing context from scope to office-hours

When you run `/office-hours` in gstack, paste the **"The one job"** line from your
`/prototype-scope` output as the product description. This ensures gstack's planning
starts from the validated founder strategy, not from vague intent.

Example:
```
/office-hours

"Take a seed-stage founder's Stripe and Mercury credentials and produce a
pre-filled investor update template with a source citation for every number."
[riskiest assumption: founders will trust AI-gathered numbers with source attribution
enough to send them to investors without double-checking]
```

gstack's `/office-hours` will push back on the framing, challenge premises, and
produce a design doc. That's intentional — it is the stress-test of your scope
from an engineering standpoint, the same way `/synthetic-customer-panel` was the
stress-test from a customer standpoint.

### What /prototype-review looks for after a gstack sprint

When you return to `founding-with-claude` and run `/prototype-review`, look for the
following gstack artifacts in your product repo:

- **The PR** from `/ship` — does what was shipped match what was scoped?
- **The `/review` findings** — were there completeness gaps that affect the prototype thesis?
- **The `/qa` bug log** — what broke in real browser testing? Was any of it related to the riskiest assumption?
- **Test coverage from `/ship`** — is the prototype behavior actually tested?

---

## The weekly review loop

The founder runs two weekly reviews:

| Review | Skill | Covers |
|--------|-------|--------|
| Engineering retrospective | gstack `/retro` | What shipped, test health, team streaks |
| Founder review | `/weekly-founder-review` | What was learned, user signals, the one thing |

Run them in order: `/retro` first (engineering facts), then `/weekly-founder-review`
(founder judgment). The retro gives you the "what was shipped" section for the
founder review, grounded in actual git history rather than memory.

---

## The `/office-hours` vs `/product-strategy-brief` distinction

Both skills interrogate a product idea. They operate at different levels:

| | gstack `/office-hours` | founding-with-claude `/product-strategy-brief` |
|---|---|---|
| **Input** | A product or feature idea | Opportunity memo + customer synthesis + panel output |
| **Lens** | Engineering and product (what to build) | Customer and market (why to build it) |
| **Forces** | Implementation alternatives, scope, feasibility | Target customer, riskiest assumption, what not to build |
| **Output** | Design doc for the engineering sprint | One-page brief gating the prototype |
| **When** | During the build sprint (after strategy is set) | Before the build sprint (after customer discovery) |

Run `/product-strategy-brief` first. Feed the output into `/office-hours`.
They are sequential, not alternatives.

---

## Security: `/cso` after the prototype

gstack's `/cso` skill runs an OWASP Top 10 + STRIDE threat model against the codebase.
Run it after the prototype sprint if:

- The prototype handles user credentials (API keys to Stripe, Mercury, etc.)
- The prototype will be shown to real users with real data
- You are preparing for fundraising and expect investor security questions

This is not part of `/prototype-review` by default — add it explicitly if the
prototype handles sensitive data.

---

## Installing both

gstack installs globally (once per machine). `founding-with-claude` is a project
repo you clone and open in Claude Code.

```bash
# 1. Install gstack globally (one time)
# Open Claude Code and paste:
# Install gstack: run git clone --single-branch --depth 1 \
#   https://github.com/garrytan/gstack.git ~/.claude/skills/gstack \
#   && cd ~/.claude/skills/gstack && ./setup

# 2. Clone founding-with-claude
git clone https://github.com/sinned/founding-with-claude
cd founding-with-claude
claude

# Now both are available:
# - founding-with-claude skills from the project .claude/skills/
# - gstack skills from the global ~/.claude/skills/gstack/
```

When you are in the `founding-with-claude` repo, you will have access to all 13
founder skills. When you open your product repo for the build sprint, you will have
access to all gstack skills. The two sets coexist without conflict.

---

## Which to use for prototyping AI features

You have two prototyping options for the build sprint:

| | prototype-with-claude | gstack |
|---|---|---|
| **Best for** | Prototyping AI agent behaviors (skills) | Full product feature development |
| **Workflow** | Write SKILL.md → eval → improve → export to Python | /office-hours → /autoplan → /review → /qa → /ship |
| **Output** | Validated Claude skill + optional SDK Python | Shipped PR with tests and QA sign-off |
| **When to use** | Your prototype IS an AI agent behavior | Your prototype is a product feature that may use AI |

Use `prototype-with-claude` when the thing you are prototyping is the AI behavior itself
(like the investor update data-gathering skill). Use gstack when you are building a product
feature that may or may not use AI (like the web app that wraps the skill and presents
it to users).

In many Week 5 build sprints, you will use both: `prototype-with-claude` to validate the
AI behavior, gstack to build and ship the product wrapper around it.

---

## For Anthropic reviewers

The relationship between gstack and `founding-with-claude` demonstrates the skills
pack pattern at scale: two independent packs, each focused on a specific professional
context, designed to be composed rather than competing.

gstack is the engineering operations layer. `founding-with-claude` is the company-building
strategy layer. Together, they cover the full founder journey — from finding a problem
to shipping a product that solves it to raising money based on evidence that it works.

A founder with both installed in Claude Code has, in effect, a virtual team across every
phase of company building.
