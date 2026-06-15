# Product Strategy Brief — Example Output

*Condensed example from the investor update automation use case.*
*Full context in `work/product-strategy-brief/product-brief-output.md`.*

---

# Product Strategy Brief
*Generated: 2026-06-14 | Stage: pre-prototype*

## Target customer
**Who:** Seed-stage founder, typically solo or with 1 co-founder, 0-15 employees
**When:** Sunday evening, writing their weekly investor update
**What they feel:** Dreading the 90-minute data gathering before they can write
a word. Afraid of sending a wrong number to investors.

## Core problem
Seed-stage founders spend 90+ minutes gathering metrics from 4-6 sources before
they can write a 30-minute investor update, because there is no tool that reliably
gathers, attributes, and formats their key metrics in one place.

## Solution hypothesis
We believe seed-stage founders would use UpdateDraft when sitting down to write
their weekly investor update to pull their Stripe, Mercury, and Linear data into
a pre-filled template with source attribution for every number, so they can send
to investors without manually verifying.

## Key bets

| Bet | Confidence | How we validate |
|-----|-----------|-----------------|
| Founders will trust source-attributed numbers without checking | Low | Show it to 3 founders with real accounts |
| The format is stable enough to template | High | Confirmed: 6/7 interviews said format never changes |
| Stripe + Mercury covers 80%+ of what founders need | Medium | Check what integrations users ask for first |

## What we are NOT building (v0)
- Writing the narrative (founders want to write it themselves)
- Linear integration (API complexity not worth it for v0)
- Email sending (out of scope — just produce the doc)

## Riskiest assumption
Founders will trust AI-gathered numbers with source attribution enough to send
them to investors without double-checking.

## Prototype success criteria
A founder can go from "no data pulled" to "pre-filled template with source links"
in under 5 minutes, AND at least 2 of 3 test users say they would send the output
without going back to verify the numbers in Stripe.
