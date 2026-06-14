# Prototype Scope — Full Example Output

*See `.claude/skills/prototype-scope/examples/example-output.md` for the condensed version.*
*This is the full output as saved by /prototype-scope.*

---

# Prototype Scope
*Generated: 2026-06-14 | Time budget: 5 days | Product: UpdateDraft*

## The riskiest assumption being tested
Founders will trust AI-gathered numbers with source attribution enough to send
them to investors without going back to manually verify in Stripe or Mercury.

This assumption, if false, means the product needs a fundamentally different
design — perhaps a "suggest and verify" mode rather than a "gather and present" mode.

## The one job
Take a seed-stage founder's Stripe and Mercury API credentials, pull the current
week's key metrics, and produce a pre-filled investor update template with a source
citation for every number.

## Inputs
1. Stripe API key (read-only scope: see all charges and subscriptions)
2. Mercury API key (read-only scope: see balance and transactions)
3. Optional: founder's existing update template (defaults to the standard 5-section format)

## Outputs
A Markdown file at `output/investor-update-[date].md` with:
- Pre-filled metrics for all standard sections
- Inline source tags: `[$12,400 MRR — Stripe, 2026-06-14 11:02pm]`
- Empty narrative sections with prompts for the founder to fill in
- A "Sources & timestamp" footer

## In scope (v0)
- **Stripe:** MRR (current month), new revenue this week, churned revenue this week, net new ARR
- **Mercury:** Cash balance (current), estimated monthly burn (based on last 30 days of spending)
- **Calculations:** Runway estimate (cash / burn), week-over-week MRR growth
- **Format:** Standard 5-section investor update template with source tags

## Explicitly out of scope
| Out of scope | Why |
|-------------|-----|
| Linear / GitHub integration | Does not test the trust assumption; adds 2-3 days of complexity |
| Writing the narrative | Founders said they want to write it themselves (confirmed in 7/7 interviews) |
| Email sending or Notion export | No learning value in v0; adds infrastructure |
| Mixpanel / PostHog / product analytics | Nice to have but requires user auth setup; defer to v1 |
| Multi-workspace Stripe | Single account is enough to test trust assumption |
| Historical comparisons | Week-over-week is sufficient for v0 |

## Success criteria

**The prototype succeeds if:**
At least 2 of 3 live test users say they would send the output to their investors
without manually verifying the numbers in Stripe — AND they specifically cite the
source tags as the reason they trust it.

**The prototype fails if:**
All 3 test users say they would check the numbers anyway, or if any user says the
source tags feel like they are hiding something rather than proving something.

**The prototype is inconclusive if:**
Users trust the numbers but do not cite the source tags — in which case we need
to understand what is driving trust, because it is not what we designed for.

## Build time budget
- Day 1: SKILL.md creation with `/new-skill`, first working run
- Day 2-3: Eval and improve cycles (target: 80%+ eval score)
- Day 4: First live test with a real founder's Stripe and Mercury accounts
- Day 5: Second and third live tests; return to this repo for `/prototype-review`

## Readiness checklist

Before opening `../prototype-with-claude`:
- [x] Product brief is written (`examples/product-brief-output.md`)
- [x] Riskiest assumption is clearly stated (trust + source attribution)
- [x] The one job can be stated in one sentence ✓
- [x] At least one real test case exists (my own Stripe account + expected MRR)
- [x] Time budget is set: 5 days

## Handoff to prototype-with-claude

When you open `../prototype-with-claude`:

1. Run `/new-skill` — when asked "what is the job?", say:
   > "Pull a founder's Stripe MRR, new revenue, churn, Mercury cash balance,
   > and burn rate. Produce a Markdown investor update template with source
   > attribution for every number in the format: [$X — Stripe, pulled at Y time]."

2. When asked "what does success look like?", use this:
   > "A founder can go from 'no data' to 'pre-filled template with source tags'
   > in under 5 minutes, and would say they trust the numbers enough to send them."

3. First eval test case: run it against your own Stripe account. Every number
   should match Stripe's MRR dashboard within $1.

4. Run `/eval-skill generate-investor-update` after your first pass.

5. Return here and run `/prototype-review` when you have working output.
