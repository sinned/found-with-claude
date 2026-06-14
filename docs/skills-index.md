# Skills Index

All 13 skills in this pack, with description, input, output, and phase.

---

## `/founder-opportunity-map`

**Phase:** Problem discovery (Step 1)
**When to use:** At the start of a new venture, or when re-evaluating what to work on

**Input:** Founder's background, domain expertise, hunches, messy notes
**Output:** Ranked opportunity memo with 3-6 areas scored on pain, underservice, and founder fit

**Key outputs:**
- `examples/opportunity-memo-output.md`

**Template:** `.claude/skills/founder-opportunity-map/templates/opportunity-memo.md`

---

## `/customer-discovery-synthesizer`

**Phase:** Customer discovery (Step 2)
**When to use:** After 2+ customer interviews — more is better

**Input:** Raw interview notes, transcripts, voice memo summaries
**Output:** Synthesis: patterns, jobs-to-be-done, quotes, riskiest assumption, open questions

**Key outputs:**
- `examples/customer-synthesis-output.md`

**Template:** `.claude/skills/customer-discovery-synthesizer/templates/interview-guide.md`

---

## `/synthetic-customer-panel`

**Phase:** Customer simulation (Step 3)
**When to use:** Before writing a product brief or prototyping — to stress-test a concept

**Input:** Customer synthesis + concept to test
**Output:** 4-6 archetype reactions, cross-panel analysis, hypotheses to test

**Key outputs:**
- `examples/synthetic-customer-panel-output.md`

**Caution:** Simulation tool only. See `docs/using-simulation-responsibly.md`.

---

## `/product-strategy-brief`

**Phase:** Product strategy (Step 4)
**When to use:** When ready to define what to build — before opening any code

**Input:** Opportunity memo + customer synthesis + panel output
**Output:** One-page brief: target customer, core problem, solution hypothesis, key bets, out-of-scope

**Key outputs:**
- `examples/product-brief-output.md`

---

## `/prototype-scope`

**Phase:** Prototype planning (Step 5)
**When to use:** Before opening the build environment

**Input:** Product strategy brief
**Output:** Prototype scope document, success criteria, readiness checklist, handoff to prototype-with-claude

**Key outputs:**
- `examples/prototype-scope-output.md`

**References:**
- `.claude/skills/prototype-scope/references/prototype-with-claude.md`

---

## `/prototype-review`

**Phase:** Prototype evaluation (Step 5)
**When to use:** After completing a build sprint in prototype-with-claude

**Input:** Prototype scope + product brief + what was actually built
**Output:** Honest verdict (Proven / Disproven / Inconclusive / Blocked) + next steps

**Key outputs:**
- `examples/prototype-review-output.md`

---

## `/first-users-outreach`

**Phase:** Early user acquisition (Step 6)
**When to use:** When ready to find the first 10 users

**Input:** Product brief + prototype description
**Output:** Outreach messages (warm, referral, cold) + onboarding ask + feedback capture guide

**Key outputs:**
- `examples/first-users-outreach-output.md`

---

## `/pmf-signal-review`

**Phase:** PMF sprint (Step 7)
**When to use:** After 10+ users, to assess whether the signals indicate product-market fit

**Input:** User data, feedback, retention signals, qualitative observations
**Output:** Signal memo with verdict (Strong / Mixed / Weak) and next steps

**Key outputs:**
- `examples/pmf-signal-review-output.md`

---

## `/growth-experiment-backlog`

**Phase:** Growth (Step 8)
**When to use:** When you have early PMF signals and want to grow systematically

**Input:** PMF signal memo + current bottleneck
**Output:** Prioritized backlog of 3 experiments to run this week + full backlog

**Key outputs:**
- `examples/growth-experiment-backlog-output.md`

---

## `/founder-hiring-scorecard`

**Phase:** Hiring (Step 9)
**When to use:** Before starting any hiring process for an early-stage role

**Input:** Role description + team context + what this hire must unlock
**Output:** Hiring scorecard with must-haves, nice-to-haves, red flags, and interview questions

**Key outputs:**
- `examples/hiring-scorecard-[role].md`

---

## `/fundraising-narrative`

**Phase:** Fundraising (Step 10)
**When to use:** When you have real traction and are preparing to raise

**Input:** Product brief + PMF signal review + traction data
**Output:** Investor memo + objection map

**Key outputs:**
- `examples/fundraising-narrative-output.md`

**Timing note:** Do not run this without real traction. A narrative without traction
is a hypothesis presentation.

---

## `/demo-day-script`

**Phase:** Demo Day (Step 11)
**When to use:** When preparing for a high-stakes 2-minute pitch

**Input:** Fundraising narrative + live demo flow
**Output:** Word-for-word 2-minute script with timing guide and danger zones

**Key outputs:**
- `examples/demo-day-script-output.md`

---

## `/weekly-founder-review`

**Phase:** Ongoing
**When to use:** Every Friday (or Monday morning)

**Input:** What happened — wins, blocks, conversations, data, personal state
**Output:** Structured weekly review: what was learned, what was done, what was heard, what to do next

**Key outputs:**
- `examples/weekly-review-[date].md`

**Template:** `.claude/skills/weekly-founder-review/templates/weekly-founder-review.md`

---

## Skill chain (the recommended sequence)

```
/founder-opportunity-map
        ↓
/customer-discovery-synthesizer
        ↓
/synthetic-customer-panel
        ↓
/product-strategy-brief
        ↓
/prototype-scope → [prototype-with-claude] → /prototype-review
        ↓
/first-users-outreach
        ↓
/pmf-signal-review
        ↓
/growth-experiment-backlog
        ↓  (in parallel)
/founder-hiring-scorecard
        ↓
/fundraising-narrative
        ↓
/demo-day-script

(ongoing throughout)
/weekly-founder-review
```

Each skill's output is the next skill's input. Run them in order for the full
journey. Jump in at any phase if you are already past the earlier ones.
