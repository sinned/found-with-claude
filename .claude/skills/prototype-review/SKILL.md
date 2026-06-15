---
name: prototype-review
description: Review a built prototype against the original strategy and scope. Produces an honest assessment of whether the prototype proves or disproves the key thesis. Use after completing a build sprint in prototype-with-claude. Trigger phrases: "review the prototype", "did we build the right thing", "evaluate what we built", "prototype debrief".
---

# Prototype Review

Takes the prototype scope, the product strategy brief, and the actual prototype
output (or description of what was built) and produces an honest assessment:
did the prototype test what it was supposed to test, and what did we learn?

## Input

Look for:
- `work/[startup]/product/prototype-scope.md` — from `/prototype-scope`
- `work/[startup]/product/strategy-brief.md` — from `/product-strategy-brief`
- Evidence of what was built (one of these):
  - Output files from the prototype itself
  - A description of what was built from the founder
  - Eval reports from `https://github.com/sinned/prototype-with-claude/output/evals/`
  - The SKILL.md that was created in `https://github.com/sinned/prototype-with-claude/.claude/skills/`

If the founder has not built anything yet, stop and say: "Run this review after
you have something to show. If you have not started building, run `/prototype-scope` first."

## Steps

1. **Read the original scope and brief** — Understand what was supposed to be built
   and what assumption it was supposed to test.

2. **Understand what was actually built** — From the founder's description, output files,
   or the prototype-with-claude output directory.

3. **Assess scope alignment:**
   - Did the prototype cover what was in scope?
   - Did it include anything that was explicitly out of scope?
   - If scope changed during the build, why?

4. **Evaluate against success criteria:**
   - Does the prototype meet the stated success criteria?
   - If not, which criteria did it fail and why?

5. **Assess the riskiest assumption:**
   - Was the riskiest assumption actually tested?
   - What did the prototype reveal about it?
   - Was the assumption confirmed, disproved, or still unclear?

6. **Identify what the prototype revealed that was unexpected:**
   - What did you discover during the build that you did not anticipate?
   - What new questions did it raise?

7. **Give an honest verdict:**
   - Proven: the prototype demonstrates the core thesis and is worth showing to users
   - Disproven: the prototype revealed the thesis is wrong — pivot the strategy
   - Inconclusive: the prototype worked but did not test the right thing — rescope
   - Blocked: the prototype could not be built as scoped — need to change approach

8. **Write the review** — Follow the output format below.

9. **Save output** — Write to `work/[startup]/product/prototype-review.md`.

## Output format

```markdown
# Prototype Review
*Generated: [date] | Verdict: [PROVEN / DISPROVEN / INCONCLUSIVE / BLOCKED]*

## What was scoped vs. what was built

| Scope item | Built? | Notes |
|------------|--------|-------|
| [In-scope item 1] | ✅ Yes | |
| [In-scope item 2] | ⚠️ Partial | [What was different] |
| [In-scope item 3] | ❌ No | [Why not] |

**Scope changes:** [Any explicit exclusions that were added to scope, and why]

## Success criteria assessment

| Criterion | Met? | Evidence |
|-----------|------|----------|
| [Criterion 1] | ✅ / ⚠️ / ❌ | [What we observed] |
| [Criterion 2] | | |

## The riskiest assumption: was it tested?

**The assumption:** [From the scope document]

**Was it tested?** [Yes / No / Partially]

**What the prototype revealed:**
[What we now know about this assumption that we did not know before]

**Our conclusion:**
[Confirmed / Disproven / Still unclear — and why]

## Unexpected discoveries

- [Thing we learned that we did not expect]
- [New question raised by what we built]

## Verdict: [PROVEN / DISPROVEN / INCONCLUSIVE / BLOCKED]

**PROVEN** — The prototype demonstrates [specific claim]. We should move to getting
real users. Next step: run `/first-users-outreach`.

**DISPROVEN** — The prototype revealed that [what was wrong]. The strategy needs
to change. Specifically: [what to change and why]. Next step: run
`/product-strategy-brief` with the new understanding.

**INCONCLUSIVE** — The prototype worked but did not actually test the riskiest
assumption because [reason]. We need to [what to do differently]. Next step:
run `/prototype-scope` with a tighter definition of the test.

**BLOCKED** — We could not build what was scoped because [reason]. Options:
[alternative approaches or scope changes]. Next step: [specific recommendation].

## What to do next

[Specific, actionable recommendation based on the verdict]
```

## What makes a good vs. bad prototype review

**Bad review:** "The prototype worked well and showed promise."

**Good review:** "The prototype met 4 of 5 success criteria but failed to demonstrate
that a founder could get the output in under 2 minutes from their own data. The
riskiest assumption (founders trust AI-generated numbers in investor updates) was
not tested — the prototype did not produce numbers, only prose. We need to build a
data ingestion step before we can test the real thesis."

Be honest about what was not tested. A prototype that builds confidence without
testing the riskiest assumption is a waste. Better to discover the failure now than
after 3 months of user acquisition.
