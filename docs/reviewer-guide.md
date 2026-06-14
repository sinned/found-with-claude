# Reviewer Guide

For Anthropic employees, advisors, or external reviewers evaluating this repo.

---

## What this is

`founding-with-claude` is a Claude Skills pack for startup founders. It provides
13 opinionated skills covering the full company-building loop from problem discovery
to Demo Day. It is a companion to `prototype-with-claude`, which covers the
AI feature prototyping phase specifically.

---

## What to look at first

**The skills — these are the primary artifact:**

```
.claude/skills/
├── founder-opportunity-map/SKILL.md
├── customer-discovery-synthesizer/SKILL.md
├── synthetic-customer-panel/SKILL.md
├── product-strategy-brief/SKILL.md
├── prototype-scope/SKILL.md
├── prototype-review/SKILL.md
├── first-users-outreach/SKILL.md
├── pmf-signal-review/SKILL.md
├── growth-experiment-backlog/SKILL.md
├── founder-hiring-scorecard/SKILL.md
├── fundraising-narrative/SKILL.md
├── demo-day-script/SKILL.md
└── weekly-founder-review/SKILL.md
```

Each SKILL.md follows the same format as `prototype-with-claude`:
- YAML frontmatter with `name:` and `description:`
- Input definition
- Steps (explicit, sequential)
- Output format (exact structure)
- Error handling

**The documentation:**

- `docs/founder-journey-map.md` — how the skills connect end-to-end
- `docs/prototype-with-claude-integration.md` — how this repo integrates with the sibling repo
- `docs/using-simulation-responsibly.md` — responsible use of the synthetic panel
- `docs/yc-style-demo-day-track.md` — the Demo Day preparation framework

**The journey worked examples:**

- `journeys/idea-to-demo-day.md` — the full 12-week arc
- `journeys/week-01-find-a-problem.md` — first week in detail

**The example inputs and outputs:**

- `examples/founder-context.md` — sample founder context
- `examples/customer-transcript-1.md` — sample interview transcript
- `examples/opportunity-memo-output.md` — sample skill output

---

## What to run

Open the repo in Claude Code and try these:

```
/founder-opportunity-map
```
Input: anything in `examples/founder-context.md`. Expected: structured opportunity memo.

```
/customer-discovery-synthesizer
```
Input: `examples/customer-transcript-1.md`. Expected: synthesis with patterns and quotes.

```
/weekly-founder-review
```
Input: anything about this week. Expected: structured review with clear next step.

These three skills cover the most fundamental founder use cases and are the best
entry points for evaluation.

---

## What makes this different from existing Claude for founders content

Most "AI for founders" content:
- Treats founders as developers
- Focuses on code generation and prototyping
- Stops at shipping a product

This repo:
- Treats founders as company builders
- Covers the full loop: finding problems, talking to customers, writing strategy,
  building, getting users, measuring PMF, fundraising, Demo Day
- Treats the weekly review as the core loop, not a side skill

The key thesis: most founding failures are not caused by slow coding. They are
caused by building the wrong thing, talking to the wrong customers, or writing
the wrong pitch. Claude can help with all of those.

---

## What to evaluate

**Skill quality:**
- Are the steps concrete and actionable?
- Is the output format explicit enough that Claude will produce consistent results?
- Does the skill handle missing or messy input gracefully?
- Is the description field specific enough for Claude to know when to use it?

**Journey coherence:**
- Do skill outputs chain into each other naturally?
- Is it clear what comes before and after each skill?
- Does the 12-week journey map feel realistic for a real founder?

**Simulation responsibility:**
- Does `/synthetic-customer-panel` include appropriate caveats?
- Is `docs/using-simulation-responsibly.md` honest and specific?

**Integration with `prototype-with-claude`:**
- Is the handoff between the two repos clear?
- Does `/prototype-scope` give a founder everything they need to open the sibling repo?
- Does `/prototype-review` connect the build output back to the strategy?

---

## What is deliberately missing

**Production infrastructure.** This repo does not include SDK code, APIs, or
deployment patterns. Those belong in `prototype-with-claude`. This repo is about
the founder workflow, not the technical implementation.

**Market-specific customization.** The skills are intentionally generic. A founder
building in health tech will customize the opportunity map criteria differently than
one building in developer tools. The templates are starting points, not final answers.

**Fundraising tactics.** `/fundraising-narrative` produces a narrative structure,
not tactical fundraising advice (who to email, how to work intros, what valuation
to set). Those are out of scope for a skills pack.

---

## Questions for discussion

1. Which skills would a first-time founder find most valuable vs. most confusing?
2. Are there important founder workflows missing from this list?
3. Does the weekly review skill feel like the right integrating mechanism?
4. Is the simulation responsibility framing strong enough?
5. How should this repo evolve as Claude Code capabilities change?
