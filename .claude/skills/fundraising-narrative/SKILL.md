---
name: fundraising-narrative
description: Build a fundraising narrative and investor memo from traction data and product strategy. Produces an investor memo and objection map. Use when a founder is preparing to raise. Trigger phrases: "fundraising narrative", "investor memo", "write my pitch", "prepare for fundraising", "tell the investor story".
---

# Fundraising Narrative

Takes product strategy, traction data, and PMF signals and produces an investor memo
and an objection map. This is the story investors need to hear — built from evidence,
not aspiration.

**Important timing note:** This skill works best when you have real traction to
point to. A narrative built without data is a hypothesis presentation. Run
`/pmf-signal-review` first. If the signals are weak, finish another month of
user learning before writing this narrative.

## Input

Look for:
- `work/[startup]/product/strategy-brief.md` — the core strategy
- `work/[startup]/traction/pmf-signals.md` — what the signals show
- `work/[startup]/customers/synthesis.md` — what customers said
- Specific traction numbers the founder provides in the current conversation:
  - Revenue or ARR
  - Active users and retention
  - Growth rate (week-over-week or month-over-month)
  - Any notable customers, pilots, or partnerships

If the founder has no traction yet: say so and recommend waiting. A narrative
without traction creates fundraising that, at best, gets signed term sheets
that blow up in diligence.

## Steps

1. **Extract the narrative spine** — From the strategy and traction, identify:
   - The market insight (what most people get wrong about this space)
   - The customer insight (what you learned from talking to customers)
   - The product thesis (what you built and why it works)
   - The traction proof (what has happened so far)
   - The ask (what you need and what you will do with it)

2. **Write the investor memo** — A one-page version of the narrative. Not a slide
   deck. A memo forces precision. If you cannot explain it in 600 words, you do not
   know it well enough.

3. **Build the objection map** — For each of the 5 most common investor objections
   to this type of company, write the honest answer. Not the spin — the honest answer,
   including where you do not yet have a great answer.

4. **Identify the most important question the investor will ask** — The one question
   that, if answered well, unlocks the meeting. This is usually the question you
   least want them to ask.

5. **Write the narrative** — Follow the output format below.

6. **Save output** — Write to `work/[startup]/pitch/fundraising-narrative.md`.

## Output format

```markdown
# Fundraising Narrative
*Generated: [date] | Stage: [seed / pre-seed / Series A] | Target raise: [$X]*

## The 30-second version
[3-4 sentences: problem, insight, what we built, traction. Practice saying this
out loud. If it takes more than 45 seconds, cut.]

---

## Investor Memo

### The problem
[1-2 paragraphs: what is broken and why. Specific. Who suffers and how much.
Not market size — the actual experience of the problem.]

### Why now
[1 paragraph: what has changed that makes this possible or necessary today that
was not true 5 years ago. Technology shift? Regulatory change? Behavior change?]

### Our insight
[1 paragraph: what we learned from talking to customers that most people building
in this space do not know. This is your unfair advantage — not technology, but
understanding.]

### What we built
[1 paragraph: the product and the key design choices. Why this approach vs. others.
What makes it work. Be specific.]

### Traction
[1 paragraph + specific numbers:
- Users: [N active] / [N total]
- Retention: [X% week-2 retention or equivalent]
- Growth: [X% week-over-week / month-over-month]
- Revenue: [$X MRR or ARR, if applicable]
- Notable: [Any customers, pilots, or notable signals]
]

### Why us
[1 paragraph: why this team, specifically, will win this market. Founder-market
fit. Unique access. What you have done that demonstrates you can execute.]

### The ask
[$X to reach [milestone]. Milestone: [what we will prove with this money that
makes the next round obvious. Not "grow to $1M ARR" — "prove that [specific bet]
is true by [date] with [specific evidence]."]

---

## Objection Map

| Objection | Honest answer | What we are doing about it |
|-----------|---------------|--------------------------|
| "The market is too small" | [Honest response] | [Evidence or plan] |
| "Why won't [big competitor] do this?" | | |
| "Why are you the right team?" | | |
| "The unit economics don't work at this scale" | | |
| "[Most likely specific objection to this company]" | | |

---

## The question I least want to be asked

**Question:** "[The question that reveals the biggest gap in the story]"

**Honest answer:** [Answer it honestly — if you do not have a good answer, the
narrative needs to account for that or the thesis needs more work]

**How to handle it in the meeting:** [The honest version, not the deflection]
```

## What makes a strong fundraising narrative

**Lead with the insight, not the market size.** Investors hear "the X market is
$Y billion" 50 times a day. They do not hear "every sales ops person I talked to
said the same thing, and no one has built for it because everyone else is building
for VPs." The insight is the hook.

**Let the traction speak.** If you have strong signals, put them in the memo first.
If you do not have strong signals, do not hide them — name them and explain what
you are doing to build them.

**The honest objection map.** Investors will find the holes in your story. If you
find them first and address them honestly, you come across as self-aware and rigorous.
If investors find holes you tried to hide, you come across as either naive or dishonest.

## What this skill does NOT produce

- A slide deck (generate from the memo)
- A list of investors to reach out to (that is tactical, not narrative)
- Valuation guidance (this depends on market conditions, comparables, leverage)
- A term sheet negotiation guide (out of scope)
