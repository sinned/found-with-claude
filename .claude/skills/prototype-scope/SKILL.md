---
name: prototype-scope
description: Define the minimum prototype scope from a product strategy brief. Produces a clear prototype scope document, success criteria, and readiness checklist — then hands off to the prototype-with-claude build environment. Use when a founder is ready to build. Trigger phrases: "scope the prototype", "what should we build first", "define the MVP", "write the prototype scope".
---

# Prototype Scope

Takes a product strategy brief and produces a prototype scope document: what to build,
what to skip, success criteria, and a readiness checklist for the build sprint.

After running this skill, the founder opens their product repo and builds. Two paths:

**Path A — Full product feature:** Use gstack (`/office-hours` → `/autoplan` → build
→ `/review` → `/qa` → `/ship`). Best when building a product feature, not just an
AI behavior. See `docs/gstack-integration.md`.

**Path B — AI behavior prototyping:** Open `https://github.com/sinned/prototype-with-claude` and use `/new-skill`
to write and validate a Claude skill. Best when the prototype IS the AI behavior.
See `references/prototype-with-claude.md`.

## Input

Primary input: `work/[startup]/product/strategy-brief.md` (from `/product-strategy-brief`)

Also useful:
- `work/[startup]/customers/synthesis.md` — to confirm which customer behavior to demonstrate
- Any constraints the founder mentions (time, team size, technical stack)

If no product brief exists, stop and say: "Please run `/product-strategy-brief` first.
A prototype scope without a strategy brief will produce the wrong thing."

## Steps

1. **Extract the riskiest assumption** — From the product brief, identify the one
   assumption that the prototype must test. Everything in the prototype scope should
   serve testing this assumption.

2. **Define the one job** — What is the single job the prototype does? If you cannot
   state it in one sentence, the scope is too broad.

3. **Define minimum inputs and outputs** — What does a user provide? What does the
   prototype produce? Be specific about format, not just concept.

4. **Scope what to include (v0)** — List only what is necessary to demonstrate
   the core job. Nothing more.

5. **List what to explicitly exclude** — Everything that would be in v1 or later.
   For each exclusion, write why: "Not in scope because it does not test the
   riskiest assumption" or "Not in scope because it would take more than [X days]."

6. **Define success criteria** — What observable outcome would prove the prototype
   works? What would prove it does not?

7. **Write the prototype readiness checklist** — What must be true before the
   founder opens `https://github.com/sinned/prototype-with-claude` and starts building?

8. **Write the handoff note** — Specific instructions for what to do when they
   open the sibling repo.

9. **Write the scope document** — Follow the output format below.

10. **Save output** — Write to `work/[startup]/product/prototype-scope.md`.

## Output format

```markdown
# Prototype Scope
*Generated: [date] | Time budget: [X days]*

## The riskiest assumption being tested
[The one thing from the product brief that must be proven by this prototype]

## The one job
[One sentence: what the prototype does]
*Example: "Takes a founder's Stripe + Linear data and drafts a weekly investor update."*

## Inputs
- [Exactly what the user provides]

## Outputs
- [Exactly what the prototype produces — format, location, structure]

## In scope (v0)
- [Feature/behavior 1 — keep it small]
- [Feature/behavior 2]

## Explicitly out of scope
| Out of scope | Why |
|-------------|-----|
| [Feature A] | Does not test the riskiest assumption |
| [Feature B] | Adds >2 days of complexity |

## Success criteria

**The prototype works if:**
[Specific, observable outcome — not "users like it" but "user X can do Y in <Z minutes"]

**The prototype fails if:**
[What failure looks like — be honest]

## Build time budget
[Honest estimate: X hours of Claude Code time]

## Readiness checklist

Before opening `https://github.com/sinned/prototype-with-claude`:
- [ ] Product brief is written and reviewed
- [ ] Riskiest assumption is clearly stated
- [ ] The one job can be stated in one sentence
- [ ] At least one real test case exists (real input → expected output)
- [ ] Time budget is set and committed

## Handoff to the build environment

### Path A: Full product feature (use gstack)

If building a product feature (a web app, API, CLI, etc.):

1. Open your product repo in Claude Code (gstack must be installed globally)
2. Run `/office-hours` — paste the "one job" line from this scope document
3. Run `/autoplan` — full CEO + design + eng review pipeline
4. Implement the plan
5. Run `/review` → `/qa` → `/ship`
6. Return here and run `/prototype-review`

See `docs/gstack-integration.md` for how to pass context from this scope into `/office-hours`.

### Path B: AI behavior prototype (use prototype-with-claude)

If the prototype IS an AI agent behavior (a Claude skill):

1. Open `https://github.com/sinned/prototype-with-claude` in Claude Code
2. Run `/new-skill` — paste the "one job" and success criteria from this document
3. Run `/eval-skill` after your first pass
4. Run `/improve-skill` to fix failures
5. Return here and run `/prototype-review`

See `.claude/skills/prototype-scope/references/prototype-with-claude.md` for more context.
```

## What a good prototype scope looks like

**Too broad:** "Build a founder OS that helps with investor updates, board prep, and
team communication."

**Too narrow:** "Auto-format a Stripe export as a table."

**Just right:** "Take a founder's raw weekly notes and Stripe MRR number and produce
a 250-word investor update with the four standard sections (highlights, metrics,
asks, next week)."

The right scope: one job, demo-able in 5 minutes, testable against a real example.

## Time constraints

If the founder says they have 1 day: scope for 3-4 hours of build time.
If they have 1 week: scope for 2-3 days of build time.
Always leave buffer — the first version is never done when you think it will be.
