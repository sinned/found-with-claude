---
name: product-strategy-brief
description: Produce a one-page product strategy brief synthesizing opportunity research, customer discovery, and concept simulation into a clear build decision. Use when a founder is ready to decide what to build. Trigger phrases: "write my product brief", "what should we build", "define our product strategy", "write the brief".
---

# Product Strategy Brief

Takes the output of problem discovery and customer research and produces a one-page
product brief: target customer, core problem, proposed solution, key bets, and what
we are NOT building.

This brief is the artifact that gates prototyping. Do not scope a prototype until
you have this. If you cannot write a clear brief, you are not ready to build.

## Input

Look for prior work in:
- `work/[startup]/founder-opportunity-map/opportunity-memo-output.md` — from `/founder-opportunity-map`
- `work/[startup]/customer-discovery-synthesizer/customer-synthesis-output.md` — from `/customer-discovery-synthesizer`
- `work/[startup]/synthetic-customer-panel/synthetic-customer-panel-output.md` — from `/synthetic-customer-panel`
- Any additional context from the founder in this conversation

If the founder has not done customer discovery, say so explicitly before writing
the brief. A brief built from hunches is a hypothesis, not a strategy.

## Steps

1. **Identify the target customer** — From the synthesis, who is the specific person
   with the problem? Not a segment. A person: role, context, the specific situation
   in which they feel the pain.

2. **Define the core problem** — In one sentence, what is the problem? It should be
   specific enough that someone would say "yes, that is exactly my problem" or
   "no, that is not my problem." Avoid vague pain points.

3. **Describe the solution hypothesis** — What do we think the product should do?
   This is a hypothesis, not a commitment. Write it as: "We believe [target customer]
   would use [solution] to [outcome]."

4. **State the key bets** — What must be true for this to work? List 3-5 assumptions
   that, if wrong, would cause the product to fail. These are not weaknesses —
   they are the bets you are making.

5. **Define what we are NOT building** — What is out of scope? This is as important
   as what is in scope. Scope creep kills prototypes.

6. **Identify the riskiest assumption** — Of all the key bets, which one is least
   validated and most likely to be wrong? This drives the prototype design.

7. **Define success for the prototype** — What would the prototype need to demonstrate
   to prove (or disprove) the riskiest assumption?

8. **Write the brief** — Follow the output format below.

9. **Save output** — Write to `work/[startup]/product-strategy-brief/product-brief-output.md`.

## Output format

```markdown
# Product Strategy Brief
*Generated: [date] | Stage: [pre-prototype / pre-fundraising / etc.]*

## Target customer
**Who:** [Specific role and context]
**When:** [The specific situation in which they feel the problem]
**What they feel:** [The actual experience of the problem — not abstract pain]

## Core problem
[One sentence. Specific. Someone would say "yes, that's me" or "no, that's not me."]

## Why existing solutions fail
| Solution | What it does | Why it falls short |
|----------|-------------|-------------------|
| [Solution 1] | [What it does] | [Why it fails for this customer] |
| [Solution 2] | ... | ... |

## Solution hypothesis
We believe [target customer] would use [solution] when [situation] to [outcome].

**The key insight:** [What makes this different from existing solutions — the non-obvious thing]

## Key bets

| Bet | Confidence | How we validate |
|-----|-----------|-----------------|
| [Assumption 1 that must be true] | High/Med/Low | [How we test it] |
| [Assumption 2...] | | |
| [Assumption 3...] | | |

## What we are NOT building (v1)
- [Out of scope item 1 — and why]
- [Out of scope item 2...]

## Riskiest assumption
[The one bet that is least validated and most likely to be wrong]

**Why it is risky:** [Specific reason]
**What it would mean if wrong:** [Impact on the business]

## Prototype success criteria
The prototype succeeds if it demonstrates: [specific, observable outcome]
The prototype fails if: [what failure looks like — be honest]

## Open questions before building
- [ ] [Question that should be answered before scoping the prototype]
```

## What a good brief looks like vs. a bad one

**Bad:** "We're building a platform for founders to manage their company better."
**Good:** "We're building a tool for seed-stage founders to auto-generate their weekly
investor update by pulling from Stripe, Linear, and Mercury — so they stop spending
3 hours on Sundays assembling data from 6 tabs."

The test: read the target customer and core problem sections to someone. Would a
founder in that role immediately recognize themselves and say "yes, that is my problem"?
If not, keep tightening.

## If prior research is missing

If there is no customer synthesis to draw from, write a brief that is clearly labeled
as a hypothesis, not a validated strategy:

> "⚠️ This brief is based on founder hunches, not customer discovery. Treat every
> assumption as unvalidated. Run /customer-discovery-synthesizer before building."
