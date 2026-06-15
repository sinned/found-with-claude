---
name: founder-opportunity-map
description: Map and rank potential startup opportunities from a founder's hunches, domain knowledge, and observations. Use when a founder wants to explore a problem space, evaluate multiple ideas, or decide where to focus. Trigger phrases: "help me find a problem", "map my opportunities", "what should I work on", "rank my ideas".
---

# Founder Opportunity Map

Takes a founder's raw observations, hunches, and domain knowledge and produces a
structured opportunity memo — ranking problem areas by pain intensity, market
underservice, and founder fit.

## Input

Anything the founder brings: industry observations, frustrations they have seen,
problems they have personally experienced, markets they know well, or ideas they
are already considering. Look for this in:
- The current conversation
- `work/[startup]/founder-opportunity-map/founder-context.md` if it exists
- `work/[startup]/founder-opportunity-map/messy-founder-notes.md` if it exists
- Any other notes or files the founder mentions

If the founder has not provided much, ask one question: "What work or industry do
you know better than most people?" Then proceed with their answer.

## Steps

1. **Extract problem signals** — From the founder's input, identify every distinct
   problem, pain, or inefficiency mentioned. Include ones the founder mentioned
   only in passing. List them without filtering.

2. **Cluster into opportunity areas** — Group the signals into 3-6 distinct
   opportunity areas. Each area should be a real category of work that a company
   could be built around.

3. **Score each opportunity area** on three dimensions (1-5 scale):
   - **Pain intensity** — How much does this problem hurt? Is it blocking work, costing money, or just annoying?
   - **Market underservice** — Are existing solutions genuinely bad, absent, or only solving part of the problem?
   - **Founder fit** — Does this founder have unusual insight, credibility, or access in this area?

4. **Identify the insight for each area** — What does the founder know or see that
   most people building in this space do not? This is the most important question.
   No answer = weak founder-market fit.

5. **Rank the opportunities** — Sort by total score. Flag any opportunities where
   the founder fit score is very low regardless of other scores (weak founder-market
   fit is often fatal).

6. **Write the memo** — Follow the output format below.

7. **Save output** — Write to `work/[startup]/founder-opportunity-map/opportunity-memo-output.md`.

## Output format

```markdown
# Opportunity Map
*Generated: [date] | Founder: [name if provided]*

## Summary
[2-3 sentences: what domain this covers and the top-ranked opportunity]

## Opportunity Areas

### 1. [Opportunity Name] — Score: [X/15]
**Pain: [X/5] | Underservice: [X/5] | Founder fit: [X/5]**

**What the problem is:**
[2-3 sentences describing the specific pain]

**What people do today:**
[Current workarounds or existing solutions and why they fall short]

**The founder's edge:**
[What this founder knows or sees that others don't — be specific]

**Key question to answer:**
[The one thing that must be true for this to be a big opportunity]

---

### 2. [Next opportunity...]

## What to do next

**If you pursue #1:** [Specific next step — who to talk to, what to learn]
**If you are unsure between #1 and #2:** [How to decide between them]
**Before talking to customers:** [What to have a point of view on first]
```

## Notes on scoring

Do not score pain intensity based on how big the market is. Score it based on
how much the specific person with the problem suffers. A problem that costs a
specific person 10 hours a week is high-pain even if only 1,000 people have it.

Do not score founder fit based on years of experience alone. Score it based on
whether the founder has a genuine insight that others do not. A founder who has
personally suffered this problem and has a non-obvious theory of what causes it
has high founder fit.

## If input is sparse

If the founder gives very little context, surface 3 high-quality questions before
proceeding:
1. What work do you know better than most people?
2. What problem have you personally experienced that you wished was solved?
3. What do people in [their industry] complain about most?

Do not try to generate an opportunity map from nothing. A map built on no founder
context is generic and useless.
