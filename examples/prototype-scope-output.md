# Prototype Scope
*Generated: 2026-06-14 | Time budget: 5 days | Product: UpdateDraft*

---

## The riskiest assumption being tested

Founders will trust AI-gathered numbers with inline source attribution enough to
send them to investors without manually re-verifying in Stripe or Mercury.

This assumption is load-bearing for the whole product design. If it fails, "gather
and present" becomes "suggest and verify" — a completely different flow where the
founder sees each number and actively confirms it before it goes into the template.
The prototype exists to answer this question before we build anything permanent.

---

## The one job

Pull a seed-stage founder's Stripe MRR, weekly revenue movement, and Mercury cash
balance, and produce a pre-filled investor update template with an inline source
citation for every number — so the founder starts writing in under 5 minutes,
not 90.

---

## Inputs

1. **Stripe API key** — read-only scope: charges and subscriptions
2. **Mercury API key** — read-only scope: account balance and transactions
3. **Optional: existing update template** — if not provided, use the standard
   5-section format (Highlights · Metrics · Narrative · Asks · Next period)

---

## Outputs

A Markdown file at `output/investor-update-[date].md` containing:

- Pre-filled metrics section with every number sourced inline:
  `[$12,400 MRR — Stripe, pulled 2026-06-14 at 11:02pm]`
- Empty Highlights, Narrative, Asks, and Next Period sections with
  brief fill-in prompts (not AI-generated text)
- A "Sources pulled" footer: tool, timestamp, and scope used for each API call

The founder copies this file, writes in the empty sections, and sends.
They do not need to open Stripe or Mercury to write the update.

---

## In scope (v0)

**From Stripe:**
- MRR (current month, calculated from active subscriptions)
- New revenue this week (new subscriptions + expansions)
- Churned revenue this week (cancellations + contractions)
- Net new ARR this week (new − churned, annualized)

**From Mercury:**
- Current cash balance
- Estimated monthly burn (average of last 30 days of outflows)

**Calculated:**
- Runway estimate (cash ÷ burn, in months)
- Week-over-week MRR growth (% and absolute)

**Format:**
- Standard 5-section investor update template
- Inline source tags on every number
- Sources footer with timestamps

---

## Explicitly out of scope

| Out of scope | Why |
|---|---|
| Linear / GitHub integration | Adds 2–3 days of complexity; does not test the trust assumption |
| AI-written narrative sections | 7/7 interviewees said they want to write it themselves — solving a non-problem |
| Email sending or Notion export | Infrastructure with no learning value in v0; founder can copy-paste |
| Mixpanel / PostHog / product analytics | Auth setup adds friction; not in the core trust loop |
| Historical comparisons (MoM, YTD) | Week-over-week is enough to test whether founders trust a number |
| Multi-workspace Stripe accounts | Single account is sufficient for the trust test |
| Brex / other banks | Mercury covers the initial test cohort; scope Brex if Mercury auth fails |
| Board memo format | Different audience, different requirements; v2 |

---

## Success criteria

**The prototype succeeds if:**
At least 2 of 3 live test users — running it against their own real Stripe and
Mercury accounts — say they would send the output to their investors without
opening Stripe to double-check. AND they specifically mention the source tags
as the reason they feel comfortable doing so.

**The prototype fails if:**
All 3 test users say they would verify anyway, OR any user says the source tags
feel like they are obscuring something rather than proving it.

**Inconclusive:**
Users are comfortable with the output but don't mention source tags. This means
something else is driving trust (or killing skepticism). We need to probe what
that is before concluding the assumption is validated.

---

## Build time budget

| Day | Work |
|-----|------|
| 1 | Write SKILL.md with `/new-skill`; first working run against real Stripe account |
| 2–3 | Eval and improve cycles; target 80%+ eval score against known test data |
| 4 | First live test with a founder's real accounts; observe, do not coach |
| 5 | Second and third live tests; return here and run `/prototype-review` |

Total: ~15 hours of focused Claude Code time.

---

## Readiness checklist

Before opening `https://github.com/sinned/prototype-with-claude`:

- [x] Product brief is written (`examples/product-brief-output.md`)
- [x] Riskiest assumption is clearly stated: trust + source attribution
- [x] The one job can be stated in one sentence ✓
- [x] At least one real test case exists: founder's own Stripe account, known MRR
- [x] Time budget is committed: 5 days
- [ ] Mercury API access confirmed (check developer.mercury.com — may require business account)
- [ ] Stripe test mode data prepared as a safe eval fixture

---

## Handoff to the build environment

This prototype IS an AI behavior, not a product feature UI. Use **Path B.**

### Path B — AI behavior (prototype-with-claude)

1. Open `https://github.com/sinned/prototype-with-claude` in Claude Code

2. Run `/new-skill` — when asked "what is the job?", paste this exactly:

   > "Pull a seed-stage founder's Stripe MRR, new revenue this week, churned revenue
   > this week, net new ARR, Mercury cash balance, and estimated monthly burn rate.
   > Produce a Markdown investor update template pre-filled with those numbers, where
   > every number has an inline source tag in the format:
   > `[$12,400 MRR — Stripe, pulled 2026-06-14 at 11:02pm]`.
   > Leave the Highlights, Narrative, Asks, and Next Period sections empty with
   > brief fill-in prompts. Add a Sources footer with the timestamp and API scope
   > for each data pull."

3. When asked "what does success look like?":

   > "A founder goes from no data to a pre-filled template with source tags in
   > under 5 minutes. They say they would send it to investors without checking
   > Stripe, and they cite the source tags as the reason."

4. First eval test case: run it against your own Stripe account in test mode.
   Every number should match Stripe's MRR dashboard within $1.

5. Run `/eval-skill generate-investor-update` after your first pass.

6. Run `/improve-skill` on any failures before the first live test.

7. Return here and run `/prototype-review` after the third live test session.
