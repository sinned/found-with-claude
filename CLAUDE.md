# Founding with Claude

This is a Claude Skills pack for founders building from idea to Demo Day.

## Your role in this repo

When a founder is working here, help them use the skills to do real founder work:
- Finding and validating problems
- Synthesizing customer conversations
- Pressure-testing ideas with simulated customer panels
- Writing product strategy and prototype scopes
- Planning outreach, analyzing PMF signals, running growth experiments
- Preparing for fundraising and Demo Day

Do not treat this as a coding repo. Most of the work here is strategic, qualitative,
and synthesis-heavy. Help the founder think clearly and move fast.

## Skill format

Skills live in `.claude/skills/<skill-name>/SKILL.md`. Format:

```yaml
---
name: skill-name
description: What this skill does and when to use it. Include trigger phrases.
---
```

The `description` is loaded at startup. The body loads when triggered. Keep descriptions
under 200 chars. Naming: directory name, YAML `name:`, and slash command must all match.

## How to invoke skills

Founders invoke skills with a slash command:

```
/founder-opportunity-map
/customer-discovery-synthesizer
/synthetic-customer-panel
/product-strategy-brief
/prototype-scope
/prototype-review
/first-users-outreach
/pmf-signal-review
/growth-experiment-backlog
/founder-hiring-scorecard
/fundraising-narrative
/demo-day-script
/weekly-founder-review
```

## Where to put raw material

The founder's work lives in `work/`, organized by skill:
- `work/founder-opportunity-map/` — founder context, notes, opportunity memos
- `work/customer-discovery-synthesizer/` — interview transcripts, synthesis output
- `work/synthetic-customer-panel/` — panel outputs
- `work/product-strategy-brief/` — product briefs
- `work/prototype-scope/` — scope documents
- `work/prototype-review/` — review outputs
- `work/first-users-outreach/` — outreach plans
- `work/pmf-signal-review/` — signal memos, raw data
- `work/growth-experiment-backlog/` — experiment backlogs
- `work/founder-hiring-scorecard/` — hiring scorecards
- `work/fundraising-narrative/` — investor memos
- `work/demo-day-script/` — scripts
- `work/weekly-founder-review/` — weekly reviews

Drop raw input in the relevant skill folder. Skills are designed to work from rough input.

## The prototyping handoff

When a founder reaches the prototyping phase:
1. Run `/prototype-scope` to define what to build
2. Open your product repo and use gstack (`/office-hours` → `/autoplan` → `/review` → `/qa` → `/ship`)
   — OR — open `https://github.com/sinned/prototype-with-claude` for AI behavior prototyping specifically
3. Run `/prototype-review` after the build to evaluate the result

See `docs/prototype-with-claude-integration.md` and `docs/gstack-integration.md`
for the full integration context.

## Simulation caveat

The `/synthetic-customer-panel` skill simulates customer reactions. It is a thinking tool,
not a research substitute. Always flag this distinction when helping a founder use it.
See `docs/using-simulation-responsibly.md`.

## Skill design principles (when helping founders build new skills)

1. One job per skill
2. Explicit output format
3. Concrete success criteria
4. Error handling in the instructions
5. Input via command invocation, not mid-run questions
