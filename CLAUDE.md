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

Each startup's work is organized by the company's knowledge corpus — not by skill:

```
work/
  .current          ← name of the active startup (e.g., "startup-1")
  startup-1/
    opportunity/    ← problem space, market analysis, founder context and notes
    customers/      ← interview transcripts, synthesis, simulated customer panels
    product/        ← strategy brief, prototype scope, build notes, prototype review
    traction/       ← outreach plans, first users, PMF signals, growth experiments
    team/           ← hiring scorecards, role definitions
    pitch/          ← fundraising narrative, demo day script
    ops/            ← weekly reviews, loop state
  startup-2/
    ...
```

Drop raw input in the most relevant folder. Skills look for input and write output
to the appropriate corpus folder (not the skill's own folder). Skills are designed
to work from rough input.

## The knowledge store

Every skill run produces two things:

1. A **working document** in `work/[startup]/[skill]/` — the full output for human review
2. **Knowledge entities** in `knowledge/[startup]/[type]/` — curated facts that accumulate over time

The knowledge store is the growing memory of this startup. It is structured for future
export to an external durable knowledge store (vector DB, document store, or API). The
schema and entity types are documented in `knowledge/README.md`.

### Knowledge store path convention

`knowledge/[startup]/[type]/[slug].md`

Resolve `[startup]` the same way as `work/` paths (read `work/.current`). The `[type]` is
one of: `insights`, `problems`, `customers`, `assumptions`, `decisions`, `signals`,
`experiments`, `people`.

### When to write to the knowledge store

After every skill run, extract the most important knowledge and write it here. Not a
summary of the output — the curated facts worth remembering across many future runs.

Write a knowledge entity when:
- A pattern appeared in 2+ interviews (→ `insight`)
- A specific pain point is identified with evidence (→ `problem`)
- A customer segment is defined in enough detail to build from (→ `customer`)
- An assumption is made explicit and should be tracked (→ `assumption`)
- A product or strategy decision is made (→ `decision`)
- A PMF signal is observed (→ `signal`)
- A growth experiment completes (→ `experiment`)

**Do not write:** vague claims, full output summaries (that is what `work/` is for),
or anything that will be overwritten on the next run.

### When to read from the knowledge store

When a skill needs context from prior runs — especially for synthesis skills that build
on prior research — read from `knowledge/[startup]/[type]/` in addition to the prior
output documents. See `knowledge/README.md` for which types each skill should read.

### The future transition

When this repo migrates to an external durable store, skill instructions change from
"write to knowledge/[startup]/[type]/[slug].md" to "POST to the knowledge API."
The entity schema (frontmatter + body format) stays the same. Only the transport changes.

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
