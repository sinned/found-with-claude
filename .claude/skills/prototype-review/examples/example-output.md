# Prototype Review — Example Output

*Week 5 review of the UpdateDraft prototype.*
*Input: prototype-scope-output.md + what was built in prototype-with-claude*

---

# Prototype Review
*Generated: 2026-06-14 | Verdict: PROVEN — partially*

## What was scoped vs. what was built

| Scope item | Built? | Notes |
|------------|--------|-------|
| Stripe MRR, new revenue, churn | ✅ Yes | Working reliably on test accounts |
| Mercury cash balance + burn rate | ✅ Yes | Works; burn rate calculation needs edge case handling |
| Source tags inline with every number | ✅ Yes | Format: `[$X — Stripe, pulled at Y time]` |
| Output as Markdown file | ✅ Yes | Saved to output/investor-update-[date].md |

**Scope changes during build:**
- Linear integration was confirmed out of scope (would have taken 2+ days)
- Added: staleness warning when Mercury API had not refreshed in 4+ hours
  (emerged from first real test when Mercury's API was delayed)

## Success criteria assessment

| Criterion | Met? | Evidence |
|-----------|------|----------|
| From "no data" to pre-filled template in under 5 minutes | ✅ Yes | Averaged 3:20 across 3 test runs |
| At least 2 of 3 test users would send without verifying | ⚠️ Partial | 2 of 3 said yes — the third (finance background) still wanted to verify |
| Users cite source tags as the reason for trust | ✅ Yes | Both users who said yes mentioned source tags explicitly |

## The riskiest assumption: was it tested?

**The assumption:** Founders will trust AI-gathered numbers with source attribution
and send them to investors without double-checking.

**Was it tested?** Yes — directly and in real conditions.

**What the prototype revealed:**
Two of three real users sent the output to their investors without verifying.
Both cited the source tags as the reason. One user (finance background) still
verified manually — but said they would "probably" stop verifying after 4-5 weeks
of consistent accuracy.

**Our conclusion:** Partially confirmed. Source attribution enables trust for most
users, but the trust threshold varies. Finance-trained founders need more time.
Early majority (community-connected, efficiency-focused) may adopt immediately.

## Unexpected discoveries

- The Mercury API sometimes lags 4-6 hours. The first test had stale balance data.
  This caused one user to briefly distrust all the numbers before we explained.
  **Implication:** Staleness warnings are a must-have, not a nice-to-have.

- One user tried to drag the output into Notion instead of their Google Doc.
  **Implication:** Consider a Notion integration before a second prototype sprint.

- Annual contract MRR calculation is a real edge case. One user's "Stripe MRR"
  was $2,400 different from their "real MRR" because of quarterly-billed annual deals.
  **Implication:** The MRR calculation logic needs to handle contract term options.

## Verdict: PROVEN — partially

The prototype demonstrated that source attribution enables trust for 2 of 3 early
test users — enough to validate the core design approach. The riskiest assumption
is partially confirmed. The edge cases discovered (staleness, annual contracts) are
solvable.

**Next step:** Move to `/first-users-outreach` and find 10 real users to use it
for 4 consecutive weeks. The 2/3 initial validation is promising; we need 4-week
retention to confirm the trust holds after the novelty wears off.

**What to fix before outreach:**
1. Staleness warning (shows "Mercury data from 2 hours ago" if API is behind)
2. Annual contract MRR option (toggle: "count annual contracts at monthly equivalent?")
3. Notion export format (one-click copy to Notion block format)
