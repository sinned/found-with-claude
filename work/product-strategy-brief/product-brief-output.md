# Product Strategy Brief — Full Example Output
*Generated: 2026-06-14 | Stage: pre-prototype | Product: UpdateDraft*

## Target customer
**Who:** Seed-stage founder, 6-18 months post-raise, 10-30 investors, no dedicated
finance person yet. Sends weekly or bi-weekly investor updates. Has Stripe for
revenue tracking and Mercury as their primary bank account.

**When:** Sunday evening, sitting down to write the investor update. Has 2 hours
before the update is due. Knows it should take 30 minutes to write but knows the
data gathering will take another 90 minutes first.

**What they feel:** Low-grade dread about the next 90 minutes. Not because the
writing is hard — they actually value the writing. Because pulling the same numbers
from the same 4 sources every week feels like admin, not founder work. And there
is always a low-level fear that a number will be wrong.

---

## Core problem
Seed-stage founders spend 90+ minutes gathering metrics from Stripe, Mercury, and
2-4 other sources before writing a 30-minute investor update — every week, for
months — because there is no tool that reliably gathers and attributes their key
metrics in one place.

*The "who would say yes / who would say no" test:*
- A seed-stage founder on Sunday evening says: "YES, that is my problem."
- A Series A founder with a finance hire says: "No, that's my finance person's problem."
- A pre-revenue founder says: "I don't have this problem yet — I just describe what I did this week."

This confirms the target is specific: seed-stage, post-revenue, pre-finance-hire.

---

## Why existing solutions fail
| Solution | What it does | Why it falls short |
|----------|-------------|-------------------|
| Zapier / Make automations | Trigger-based data pulls | Breaks on format changes; founder stops trusting it after one wrong number |
| BI tools (Looker, Metabase) | Dashboard for operational metrics | Requires data team setup; not optimized for investor update format |
| Manual + template | Copy-paste from each source | Reliable but takes 90+ minutes; not scalable across 50 investor updates |
| AI "write my update for me" tools | Draft the full update | Solves the wrong problem; founders want to write the narrative themselves |

---

## Solution hypothesis
We believe seed-stage founders would use UpdateDraft when sitting down to write
their weekly investor update to auto-pull their Stripe and Mercury data into a
pre-filled template with a source citation for every number — so they can start
writing in 5 minutes instead of 90.

**The key insight:** Founders do not want AI to write the update. They want to
write it themselves. What they want is the data, already gathered, with enough
transparency to trust it. Every competitor is automating the writing. We automate
the gathering.

---

## Key bets

| Bet | Confidence | How we validate |
|-----|-----------|-----------------|
| Source attribution is sufficient for founders to trust AI-gathered numbers | Low | Show 5 founders a prototype with source tags; ask if they'd send it |
| The update format is stable enough to template | High | 6/7 interview subjects said format never changes |
| Stripe + Mercury covers 80%+ of what founders need for the data section | Medium | Count which metrics come up in outreach; Mercury may not be universal |
| Founders value writing the narrative and would resist AI-written updates | High | 7/7 interview subjects said "I like writing it" |

---

## What we are NOT building (v1)

| Out of scope | Why |
|-------------|-----|
| AI-written narrative | Founders explicitly said they want to write it themselves |
| Linear / GitHub integration | Nice to have, but complexity doesn't test the core bet |
| Mixpanel / product analytics | Valuable, but auth setup adds friction in v0 |
| Email sending | Adds infrastructure; founder can copy-paste to their email tool |
| Multi-user / team accounts | Solo founder or two-person team is the target; teams add complexity |
| Board memo format | Different format, different audience; defer to v2 |

---

## Riskiest assumption
**Founders will trust AI-gathered numbers with source attribution and send them to
investors without manually verifying.**

**Why it is risky:** Trust failure is catastrophic for this product. If one founder
sends a wrong number to their investors because they trusted our output without
checking, we get one shot at the relationship and likely one angry person in
every founder network they are in. The trust problem is not just a UX problem —
it is a business-ending risk if we get it wrong.

**What it would mean if wrong:** The entire product design needs to change. Instead
of "gather and present," we would need "suggest and verify" — a completely different
flow where the founder sees both the gathered number AND a prompt to verify before
it goes into the template.

---

## Prototype success criteria

**The prototype succeeds if:** At least 2 of 3 live test users say they would send
the auto-gathered numbers to their investors without going back to verify in Stripe
— AND they specifically cite the source tags as what made them comfortable.

**The prototype fails if:** All 3 test users say they would check the numbers anyway,
OR any user says the source tags felt inadequate or misleading.

**Inconclusive:** Users are comfortable with the numbers but do not mention the
source tags — need to understand what else is driving trust.

---

## Open questions before building

- [ ] Does Mercury have a reliable read-only API? (check developer documentation)
- [ ] How do founders who use Brex instead of Mercury want to handle bank data?
- [ ] Should the source tag show the exact timestamp, or just "today"?
- [ ] What is the right default update template to use for unfamiliar formats?
