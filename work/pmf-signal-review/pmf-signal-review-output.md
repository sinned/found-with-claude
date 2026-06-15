# PMF Signal Review — Example Output
*Generated: 2026-06-14 | Users analyzed: 25 | Period: 6 weeks*

## Verdict: MIXED SIGNALS

Early retention is strong (70% at week 4) and 3 users have referred someone without
being asked — both encouraging signals. However, the sample size is too small to
draw confident conclusions, and no users are paying yet. The "very disappointed"
cluster is clearly identifiable but small. Recommend expanding to 50+ users before
making major product decisions.

---

## Signal summary

### Retention
| Group | Count | % of total | Notes |
|-------|-------|------------|-------|
| Active (used 2+ times in last 2 weeks) | 17 | 68% | Strong for a 6-week-old product |
| Returned but dropped off | 4 | 16% | Dropped after first use |
| Tried once, did not return | 3 | 12% | All are pre-revenue founders (wrong segment) |
| Signed up but never tried | 1 | 4% | Lost to setup friction |

### The "very disappointed" cluster
**Who they are:** Founders who send weekly updates to 20+ investors, have Stripe
and Mercury both set up, and are 6-18 months post-seed.

**What they say:**
- "I've already used it for 4 weeks and I haven't verified a number manually in the last 2"
- "This is the first Sunday I haven't dreaded the update"

**What this reveals:** The ideal customer has already passed the trust threshold
and is using the source tags as the reason. This validates the core design choice.

### Four PMF dimensions

| Dimension | Signal | Evidence |
|-----------|--------|----------|
| Retention | Strong | 70% week-4 retention; better than most SaaS at this stage |
| Word of mouth | Mixed | 3 unprompted referrals in 6 weeks — early but positive |
| Depth of use | Mixed | Most using it for the designed use case; none using it for anything unexpected yet |
| Pain clarity | Strong | Every active user can describe the exact problem in one sentence |

---

## The strongest positive signal
2 users have explicitly said they no longer manually verify numbers before sending
to investors — citing the source tags. This is the first real-world validation of
the trust thesis.

## The most concerning signal
3 of 25 users signed up and never tried it. Post-onboarding interviews reveal:
they are pre-revenue founders who do not have Stripe set up yet. They were attracted
by "investor update automation" but are not the right segment for v0.

The concern: marketing is attracting some wrong-segment users, which dilutes the
retention metric. If removed from the calculation, the active retention rate rises
to 77%.

---

## What the signals mean

The signals are encouraging for a 6-week-old product with zero paid acquisition.
Retention is strong among the right-segment users (post-seed, has Stripe + Mercury).
The trust thesis is being validated by individual users who have made it through
the critical moment (sending AI-gathered numbers to investors).

The weak signals are concentrated in wrong-segment users (pre-revenue). This is
a segmentation problem, not a product problem. The marketing and onboarding should
screen for Stripe connectivity before allowing sign-up.

---

## Recommended next steps

**With MIXED SIGNALS:**

1. **Expand to 50+ users** before drawing strong conclusions — focus on right-segment
   outreach (post-seed founders with active Stripe accounts)

2. **Add Stripe-connectivity screen to onboarding** — pre-revenue founders are not
   the right v0 audience; add a "are you currently using Stripe?" check before
   allowing signup

3. **Instrument the "trust moment"** — add an in-product prompt after the first use:
   "Did you send these numbers to your investors without checking Stripe manually?"
   This makes the core signal trackable rather than requiring follow-up interviews

4. **Target the "very disappointed" cluster for referrals** — they are the right
   users to evangelize; ask each one for 2 specific referrals this week

5. **Do not write the fundraising narrative yet** — 25 users and 6 weeks is too
   thin. Get to 50+ users and 8+ weeks of retention data before telling the investor story.
