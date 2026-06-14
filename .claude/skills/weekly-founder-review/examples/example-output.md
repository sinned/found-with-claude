# Weekly Founder Review — Example Output

*Week of 2026-06-14 | Phase: Week 6 — First Users*

---

## What we learned

**Observations (what happened):**
- 4 live onboarding sessions completed this week
- 3 of 4 users sent the output to their investors without going back to Stripe
- 1 user discovered the annual contract MRR edge case (their Stripe MRR was $2,400 off)
- The Mercury API was slow on Wednesday — caused one user to briefly distrust all numbers
- 2 users asked about a Notion export format (both use Notion as their primary writing tool)

**Conclusions (what it means):**
- Source attribution is working as designed for 3/4 users — this is the strongest signal yet
- The annual contract edge case is more common than anticipated (need to probe in next 3 onboardings)
- API staleness is a trust killer — staleness warnings are non-negotiable before broader launch
- Notion is probably the right secondary integration (ahead of Google Docs)

---

## What we shipped / did

- Built and deployed the first version of UpdateDraft skill in prototype-with-claude
- Ran 4 live onboarding sessions
- Added staleness warning after the Mercury API incident (same day)
- Started a list of edge cases for the MRR calculation

---

## What we heard from users / customers

> "I actually looked at the source link and it linked directly to the Stripe transaction.
> That's when I stopped worrying." — User #2

> "I want to paste this into Notion, not Google Docs. Is that possible?" — User #3

> "My MRR on Stripe says $31,200 but my real MRR is $33,600. There are 2 annual deals
> that Stripe is not counting right." — User #4

**Signal summary:** The users who trusted it, trusted it because of the source links.
The user who didn't trust it had a legitimate edge case (annual contracts). This is
a solvable technical problem, not a trust problem.

---

## The surprise

User #2 opened the Stripe source link. I designed the source tags for credibility,
not for actual clicking. But one user actually clicked, and that's what confirmed
the numbers for them. This suggests the source links should be more prominent and
should deep-link to the specific report (not just the Stripe dashboard homepage).

---

## The most important unknown

How many founders have the annual contract MRR discrepancy? If it's more than 30%
of the target segment, we need to fix this before expanding beyond 10 users.

**How to answer it:** Ask the next 5 onboarding users: "Does your Stripe MRR match
your internal MRR calculation? If not, why not?" Track the answer.

---

## The one thing for next week

**Add the annual contract MRR toggle and deep-link the Stripe source tags to the
specific report, then do 6 more onboarding sessions.**

*Why this and not something else:* The only way to get confident on the trust thesis
is more users, but we should not onboard users with the known annual contract bug
unfixed. Fix the bug first, then onboard 6 more.

---

## Founder state

**Energy:** High
**Clarity:** Clear
**One sentence:** This is working better than I expected, and the edge cases are
making the product better rather than making me doubt the idea.

---

*Previous week's one thing:* Run 4 live onboarding sessions with real founders. ✅ Done.
