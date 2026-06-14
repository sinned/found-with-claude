# Prototype with Claude — Integration Notes

This file documents the relationship between `founding-with-claude` and its sibling
repo `../prototype-with-claude`, based on direct inspection of the sibling repo.

---

## What the sibling repo contains

`prototype-with-claude` is a starter kit for building AI-enabled product features
using Claude Code. Its core workflow:

1. **Write a SKILL.md** — a plain-text job description telling Claude what to do
2. **Run it in Claude Code** — Claude Code executes the skill interactively
3. **Eval with `/eval-skill`** — Claude-as-judge grades outputs against test cases
4. **Improve with `/improve-skill`** — Claude edits the SKILL.md to fix failures
5. **Export with `/export-to-sdk`** — generates production Python via Agent SDK

**Built-in skills (ready immediately after cloning):**
- `/qualify-lead <company>` — score a sales lead against your ICP
- `/research-agent <topic>` — produce a structured intelligence brief
- `/generate-content "<brief>"` — produce 3 content variations with recommendation
- `/qualify-lead-demo` — deliberately weak skill + saved improvement journey

**Meta-commands:**
- `/new-skill` — guided wizard to create a new skill
- `/eval-skill <name>` — run test cases and grade outputs
- `/improve-skill <name>` — edit SKILL.md to fix eval failures
- `/export-to-sdk` — generate production Python from a working skill

**Supporting resources:**
- `WALKTHROUGH.md` — complete 20-minute lead qualifier build-along
- `docs/founder-use-cases.md` — 5 startup use cases with build guides
- `docs/skill-patterns.md` — design patterns for the three skill shapes
- `docs/sdk-migration-guide.md` — how to graduate skills to production
- `docs/demo-improvement-journey.md` — real before/after: 65% → 100% eval score

**Three skill patterns covered:**
| Pattern | Use for |
|---------|---------|
| Research & Synthesize | Prospect research, market briefs, competitive analysis |
| Score & Classify | Lead scoring, ticket triage, content moderation |
| Generate & Iterate | Copy variations, outreach drafts, content at scale |

---

## What founder workflow it demonstrates

The sibling repo answers the question: **"How do I build an AI feature before
I know if it works?"**

The answer: write the behavior as a SKILL.md, validate it with Claude Code and
evals, then export to production Python only after the behavior is proven. This
avoids writing SDK code that is expensive to iterate on before the core logic
is validated.

The repo is most relevant for Week 5 of the founder journey: the prototype sprint.
It shows how to build an AI-powered feature (not just a UI or a data pipeline —
but an agent that does a job) quickly and rigorously.

---

## How it fits into this skill pack

```
founding-with-claude                    prototype-with-claude
─────────────────────                   ─────────────────────
/prototype-scope                   →    /new-skill, /qualify-lead, etc.
(define what to build)                  (build and validate the behavior)

                                   →    /eval-skill, /improve-skill
                                        (measure and improve quality)

/prototype-review               ←       Validated skill + outputs
(evaluate result vs. strategy)          (the artifact of the build sprint)

/first-users-outreach           ←       /export-to-sdk
(plan user acquisition)                 (graduate to production)
```

The skill pack (`founding-with-claude`) provides the strategic frame: what problem
to solve, what to build, what success looks like, and what to do with the result.

The sibling repo (`prototype-with-claude`) provides the tactical build environment:
how to write a skill, test it, improve it, and ship it.

---

## Which skills should reference it

- **`/prototype-scope`** — references the sibling repo as the destination after scoping.
  The prototype scope document should include a note to open `../prototype-with-claude`
  and use `/new-skill` to start building.

- **`/prototype-review`** — references the sibling repo's output (the validated skill and
  eval report) as the primary input. The review compares actual prototype behavior against
  the original scope and strategy.

**Both skills include a `references/prototype-with-claude.md` file** that gives the
founder context on what they will find when they open the sibling repo.

---

## What a founder should use it for

Open `../prototype-with-claude` when you have:
1. A completed `/prototype-scope` document (from this repo)
2. A clear answer to: "What is the one job the prototype should do?"
3. A test case in mind: "If the prototype does this for this input, it works"

Then in `prototype-with-claude`:
1. Run `/new-skill` to scaffold the skill
2. Write the SKILL.md from your scope document
3. Run the skill on your test case
4. Run `/eval-skill` to measure quality
5. Run `/improve-skill` until it passes
6. Run `/export-to-sdk` if you need a production version

Return to `founding-with-claude` and run `/prototype-review` when you have
working skill output to evaluate against the original strategy.

---

## What an Anthropic reviewer should inspect

In `prototype-with-claude`:
- `WALKTHROUGH.md` — the complete end-to-end build-along (best entry point)
- `.claude/skills/qualify-lead/SKILL.md` — the canonical well-designed skill
- `output/evals/qualify-lead-report.md` — what an eval report looks like
- `docs/demo-improvement-journey.md` — before/after skill improvement with diffs

In `founding-with-claude`:
- `.claude/skills/prototype-scope/SKILL.md` — the handoff into the sibling repo
- `.claude/skills/prototype-review/SKILL.md` — the handoff back from the sibling repo
- `.claude/skills/prototype-scope/references/prototype-with-claude.md` — integration note

---

## What could be improved next

1. **A cross-repo workflow guide** — a single document that walks a founder through
   both repos in sequence, from problem discovery to production skill.

2. **A shared ICP/context file** — a standard format for founder context that both
   repos can read, so the lead qualifier in `prototype-with-claude` knows the same
   customer profile that informed the product strategy in `founding-with-claude`.

3. **Eval templates for founder skills** — the sibling repo has a strong eval loop
   for AI behavior skills. The founder skills here could benefit from similar
   eval/improve cycles (e.g., does the opportunity memo actually surface actionable
   insights?).

4. **A portfolio view** — a skill that reads across all the artifacts produced by
   both repos (opportunity memo, synthesis, prototype eval report, PMF signals) and
   produces a one-page founder state-of-the-company briefing.
