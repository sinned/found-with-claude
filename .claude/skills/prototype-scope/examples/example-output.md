# Prototype Scope — Example Output

*Condensed example from the investor update automation use case.*

---

# Prototype Scope
*Generated: 2026-06-14 | Time budget: 5 days*

## The riskiest assumption being tested
Founders will trust AI-gathered numbers with source attribution enough to send
them to investors without double-checking.

## The one job
Take a seed-stage founder's Stripe and Mercury credentials and produce a pre-filled
investor update template with a source citation for every number.

## Inputs
- Stripe API key (read-only)
- Mercury API key (read-only)
- Update template (the founder's existing format or the default template)

## Outputs
- A Google Doc (or Markdown file) with pre-filled metrics and inline source tags
  e.g., "MRR: $12,400 [Stripe, pulled 2026-06-14 at 11:02pm]"

## In scope (v0)
- Stripe: MRR, new revenue this week, churn this week
- Mercury: current cash balance, estimated burn rate
- Source attribution inline with every number
- Output as Markdown file the founder can copy into their update

## Explicitly out of scope
| Out of scope | Why |
|-------------|-----|
| Linear integration | API complexity; does not test the trust assumption |
| Writing the narrative | Founders want to write it themselves |
| Email sending | Adds infrastructure complexity with no learning value |
| Multi-workspace support | Single account is enough to test the assumption |

## Success criteria
**Works if:** 2 of 3 test founders say they would send the output without going
back to verify numbers in Stripe — citing the source tags as the reason.

**Fails if:** All 3 test founders say they would check anyway, or the source
tags are not trusted.

## Handoff to prototype-with-claude
1. Open `https://github.com/sinned/prototype-with-claude` and run `/new-skill`
2. Name the skill `generate-investor-update`
3. Use this scope document when Claude asks "what is the job?"
4. Test case for evals: a founder with a live Stripe account producing a
   pre-filled template where every number matches Stripe's dashboard
