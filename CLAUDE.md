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

New founder? Start here:
```
/new-startup   ← sets up your workspace
/loop          ← runs autonomously from here; stops when it needs you
```

`/loop` chains all skills in sequence, running what it can and pausing with
exact instructions when it needs real-world founder input (interviews, build,
outreach, experiments). Drop the requested input and run `/loop` again to resume.

Individual skills (invoke directly if you want to jump to a specific phase):
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

## Active startup — how to resolve paths

Every founder's work lives in `work/startup-N/` where N is the startup number.

**To find the current startup before reading or writing any file:**
1. Read `work/.current` — the contents name the active startup directory (e.g., `startup-1`)
2. If `work/.current` does not exist, scan `work/` for the highest `startup-N` directory
3. If no startup directory exists, tell the founder to run `/new-startup` first

**Path convention used in all SKILL.md files:**
`work/[startup]/skill-name/filename.md`

Resolve `[startup]` using the steps above before using any path. Never hardcode a
startup number — always read `work/.current`.

## Where work lives

Each startup's work is organized by skill inside its directory:

```
work/
  .current                        ← name of the active startup (e.g., "startup-1")
  startup-1/
    founder-opportunity-map/      ← founder context, notes, opportunity memos
    customer-discovery-synthesizer/ ← interview transcripts, synthesis output
    synthetic-customer-panel/     ← panel outputs
    product-strategy-brief/       ← product briefs
    prototype-scope/              ← scope documents
    prototype-review/             ← review outputs
    first-users-outreach/         ← outreach plans
    pmf-signal-review/            ← signal memos, raw data
    growth-experiment-backlog/    ← experiment backlogs
    founder-hiring-scorecard/     ← hiring scorecards
    fundraising-narrative/        ← investor memos
    demo-day-script/              ← scripts
    weekly-founder-review/        ← weekly reviews
  startup-2/
    ...
```

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
