---
name: pmf-signal-review
description: Analyze product-market fit signals from early user data, feedback, and behavior. Produces a PMF signal memo with a clear verdict and next steps. Use when you have 10+ users and want to assess whether you are on the right track. Trigger phrases: "analyze PMF signals", "do we have product-market fit", "what do the signals say", "review our user data", "PMF check".
---

# PMF Signal Review

Analyzes early user feedback, usage patterns, retention signals, and qualitative
observations to produce a clear PMF signal memo: what the signals mean, what is
missing, and what to do next.

## Input

Bring whatever you have — not all of these are required:
- Usage data (even rough: "5 of 10 users came back a second time")
- Feedback from user conversations
- Retention signals (who came back, who did not)
- NPS or "very disappointed" survey results if available
- Qualitative observations from watching users
- Your own intuition about what is working

Put raw data in `work/[startup]/traction/` or share it in the current conversation.

If you have fewer than 5 users: note this, produce the memo with the available
signals, and recommend getting to 10+ before drawing strong conclusions.

## Steps

1. **Categorize the signals** — Separate quantitative signals (usage numbers,
   retention rates) from qualitative signals (what users said, how they behaved).

2. **Assess retention** — The core PMF signal is: do users come back? Group users:
   - Active (used it more than once in the last 2 weeks)
   - Returned but dropped off
   - Tried once, never returned
   - Never actually tried after signing up

3. **Find the "very disappointed" users** — Who are the users who would be most
   upset if the product went away? What do they have in common? This sub-segment
   is often the real target customer, even if it is different from who you expected.

4. **Identify the strongest positive signal** — What specific behavior or quote
   gives you the most confidence? This is the signal to follow.

5. **Identify the most concerning signal** — What specific behavior or absence of
   behavior worries you most? This is the signal to investigate.

6. **Assess the four PMF dimensions:**
   - **Retention** — Do users come back?
   - **Word of mouth** — Have any users told others unprompted?
   - **Depth of use** — Are users using it for more than the original use case?
   - **Pain clarity** — Do users describe a specific pain that the product solves?

7. **Give a verdict** — Honest assessment: strong signals, mixed signals, or
   weak/no signals. Do not hedge — pick one.

8. **Write the memo** — Follow the output format below.

9. **Save output** — Write to `work/[startup]/traction/pmf-signals.md`.

## Output format

```markdown
# PMF Signal Review
*Generated: [date] | Users analyzed: [N] | Period: [timeframe]*

## Verdict: [STRONG SIGNALS / MIXED SIGNALS / WEAK/NO SIGNALS]

[2-3 sentence summary of what the signals say]

---

## Signal summary

### Retention
| Group | Count | % of total | Notes |
|-------|-------|------------|-------|
| Active (used 2+ times in 2 weeks) | [N] | [%] | |
| Returned but dropped off | [N] | [%] | |
| Tried once, did not return | [N] | [%] | |
| Signed up but never tried | [N] | [%] | |

### The "very disappointed" cluster
**Who they are:** [Common characteristics of your most engaged users]
**What they say:** [Quotes or paraphrases from most engaged users]
**What this reveals:** [Why this sub-segment matters]

### Four PMF dimensions

| Dimension | Signal | Evidence |
|-----------|--------|----------|
| Retention | Strong/Mixed/Weak | [Specific data] |
| Word of mouth | Strong/Mixed/Weak/None | [Specific example or absence] |
| Depth of use | Strong/Mixed/Weak | [What users are doing with it] |
| Pain clarity | Strong/Mixed/Weak | [Can users name the problem clearly?] |

---

## The strongest positive signal
[The one thing that gives you the most confidence — be specific]

## The most concerning signal
[The one thing that worries you most — be specific and honest]

---

## What the signals mean

[3-5 sentences interpreting the signals. Not a summary — an interpretation.
What do these signals say about whether you are building the right thing
for the right person?]

---

## Recommended next steps

**If STRONG SIGNALS:**
- [What to do to deepen the signal — more users, more data]
- [What to build next to serve the most engaged users]
- [When to start the fundraising narrative conversation]

**If MIXED SIGNALS:**
- [What to investigate — which signal is most ambiguous and how to resolve it]
- [Whether to expand or narrow the target customer]
- [How many more weeks of data before drawing a conclusion]

**If WEAK/NO SIGNALS:**
- [Whether to pivot the product, the customer, or both]
- [Which assumption to go back and retest]
- [Whether to return to customer discovery]
```

## What strong PMF signals look like

From YC and startup lore, strong signals include:
- Users telling others without being asked (unprompted word of mouth)
- Users who are upset when the product is down or slow
- Users using it in ways you did not design for (depth signal)
- Users saying "this is exactly what I needed" with specific detail
- Retention above 40% week-over-week after week 2

Weak signals include:
- "It's really cool" (polite, not committed)
- High first-session time but no second session
- "I would definitely use this if it had X" (conditional — they do not use it now)
- Referrals only when directly asked

## The honest conversation

If the signals are weak: say so. The worst thing to do with weak PMF signals is
to add more features hoping the signal will improve. The right question is: "Are
we solving the right problem for the right person?" If the answer is no, the signals
will stay weak regardless of what features you add.

Return to `/customer-discovery-synthesizer` if the signals suggest you have
the wrong customer or the wrong problem.
