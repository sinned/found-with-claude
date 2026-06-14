# Fundraising Narrative — Example Output

*Example investor memo from the investor update automation use case.*
*Based on Step 10 context: 25 users, 70% retention, 3 unprompted referrals.*

---

# UpdateDraft — Investor Memo
*Seed Round | $1.2M target | June 2026*

## The 30-second version
Founders spend 3 hours gathering data before writing a 30-minute investor update.
UpdateDraft pulls that data automatically — from Stripe, Mercury, and your bank —
with a source tag for every number, so founders can send it without going back to
verify. 25 founders are using it. 70% are still using it after 4 weeks.

---

## The problem

Every founder with investors writes a weekly or bi-weekly update. The format is
always the same: key metrics, wins, problems, asks. The writing takes 30 minutes.
The data gathering takes 90-180 minutes.

Founders go to Stripe for MRR. Mercury for cash balance. Wherever they track burn.
Their project tool for what shipped. They paste everything into a Google Doc and
then do it again next week. For months. For years.

It is not that founders can't gather the data. It is that they have to do it
manually every time, from the same sources, in the same format, because there
is nothing that does it for them — and nothing they trust enough to do it for them.

## Why now

Two things are newly possible in 2026:
1. The APIs for the tools founders use (Stripe, Mercury, Linear) are mature and
   well-documented — integration is tractable at startup scale.
2. Large language models can produce formatted, source-attributed output that
   founders are willing to trust — if the output shows its work.

Three years ago, the trust problem was not solvable. Today, showing the source
and timestamp inline is enough. We validated this with 25 real users.

## Our insight

Founders do not want AI to write their investor updates. They want to write the
update themselves. What they want automated is the data gathering — specifically,
they want every number to be accompanied by where it came from and when it was pulled.

This insight inverts the obvious product design. Everyone building in this space
is automating the writing. We automate the gathering. The writing stays with the founder.
This means less AI, simpler product, faster trust.

## What we built

UpdateDraft connects to a founder's Stripe and Mercury accounts (read-only, single
OAuth flow), pulls the 6 metrics they send every week, and produces a pre-filled
investor update template. Every number shows its source: `[$12,400 MRR — Stripe,
pulled June 14 at 11:02pm]`. The founder fills in the narrative, reviews the
numbers once, and sends.

The core design choice: show the work. Not a black box. A glass box.

## Traction

- **Active users:** 25 (all organic — no paid acquisition)
- **Retention:** 70% of users have used it for 4+ consecutive weeks
- **Referrals:** 3 users referred a friend without being asked
- **NPS signal:** 4 users told us they would be "very disappointed" if we shut down
- **Revenue:** Pre-revenue; 8 users have asked about pricing

The most important signal: 2 of the first 3 users who tried it sent the AI-gathered
numbers to their investors without manually verifying them. This is the first
evidence that the trust problem is solvable.

## Why us

The two founders have combined 12 years of RevOps at B2B SaaS companies. We have
run this exact workflow at 4 companies and have personally talked to 31 founders
about it. We understand the data sources, the edge cases in the Stripe API, and
the formatting requirements that make investors happy. We are the target customer.

## The ask

$1.2M seed to:
- Build integrations for 8 additional tools (Linear, Notion, Mixpanel, Brex, etc.)
- Reach 200 active founders by Q4 2026
- Launch a paid tier at $29/month after reaching 200 users
- Prove that 60%+ of paid users retain for 3+ months

At the end of this round, we will have evidence that founders will pay for time
they get back from a workflow they hate.

---

## Objection Map

| Objection | Honest answer |
|-----------|---------------|
| "The market is too small" | The market is every startup founder with investors — approximately 50,000 active in the US at any time. At $29/month, 5,000 users = $1.7M ARR. It is a small market but a focused one with clear distribution (founder communities). |
| "Why won't Stripe build this?" | Stripe's interest is payments, not reporting. This requires integrating with Mercury, Linear, and a dozen other tools that are not Stripe's business. Stripe is not going to build a competitor to its partners. |
| "Why are you the right team?" | We have run RevOps at 4 B2B SaaS companies. We know the Stripe API better than most, and we have talked to 31 founders about this specific problem. We are not building for a customer we read about — we are the customer. |
| "What happens when Notion / Linear / Stripe build native update features?" | They build for their platform, not for founder workflows. A Stripe "investor update" feature would only include Stripe data. Our value is in integrating across tools. Single-platform features are the workaround we are replacing. |

## The question I least want to be asked

**"What does retention look like after month 3?"**

**Honest answer:** We do not know yet. Our oldest users are 6 weeks in. Retention
at 4 weeks is 70%, which is strong. Whether it stays strong at 12 weeks is the
next thing we need to prove.
