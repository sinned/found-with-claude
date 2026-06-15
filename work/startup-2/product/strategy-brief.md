# Product Strategy Brief
*Generated: 2026-06-14 | Stage: pre-prototype*

> **Provenance:** Built on the opportunity map and illustrative sample discovery in
> `work/startup-2/` (see customers/README). The riskiest bets below are not yet confirmed
> with real buyers — treat this as a strong hypothesis that gates a prototype, not a
> validated strategy.

## Target customer
**Who:** The independent crop consultant / certified crop adviser (CCA) — fee-for-service,
sells advice not product, advises dozens of growers across tens of thousands of acres.
**When:** Building or revising each grower's spray program through the season, deciding what
to recommend, at what rate, in what mode-of-action rotation — while juggling many fields in
their head.
**What they feel:** "I'm stitching the whole resistance picture together in my head and a
color-coded spreadsheet. I physically can't take on more growers without dropping quality —
and one wrong rotation that breeds resistance is my name and reputation on the line."

## Core problem
Independent crop consultants have no system that holds each field's resistance history and
catches when a spray program is stacking modes of action wrong — so their capacity is capped
by what they can keep in their own memory, and stewardship mistakes are invisible until the
weeds escape.

## Why existing solutions fail
| Solution | What it does | Why it falls short |
|----------|-------------|-------------------|
| Climate FieldView / farm-mgmt software | Maps fields, yield, as-applied data | Visualizes; doesn't reason about resistance or flag mode-of-action stacking |
| Co-op agronomy platforms | Field records tied to sales/orders | Built to transact product; conflicted; not a stewardship brain |
| Spreadsheets + the consultant's memory | Tracks resistance ad hoc | Doesn't scale, walks out the door at retirement, error-prone under pressure |
| Precision sprayers (See & Spray) | Apply chemical precisely | "A trigger finger, not a brain" — applies, doesn't decide chemistry |

## Solution hypothesis
We believe **independent crop consultants** would use **AgroGuard — a resistance-aware
decision & memory layer** when **building each grower's spray program** to **serve more acres
without quality slipping and without breeding resistance**.

It auto-ingests as-applied/spray data and field history (no manual entry), maintains a
field-by-field resistance map, and warns the consultant *before* each pass when a program
stacks modes of action — with an **explainable** recommendation they can edit and sign.

**The key insight:** The unserved layer isn't applying chemical (hardware does that) or
mapping fields (FieldView does that) — it's the *resistance reasoning* that today lives only
in expert heads. Build for the agronomist as user (not the farmer, who buys the person), and
the explainability is the product, because the consultant's reputation rides on every rec.

## Key bets

| Bet | Confidence | How we validate |
|-----|-----------|-----------------|
| The independent consultant is the right beachhead buyer (aligned incentive, can buy without committee) | Med | Buyer-discovery interviews; a paid pilot commit |
| A consultant will pay enough per seat/acre to build a business on | **Low** | Get to a real price + pilot fee in buyer interviews |
| As-applied/field data can be auto-ingested with minimal manual entry | Low | Technical spike against real equipment/software exports |
| An explainable resistance recommendation is trustworthy enough that a consultant will sign their name to it | Med | Put a prototype rec in front of a real CCA's real fields |
| The resistance "brain" is the wedge (vs logistics or knowledge-capture) | Med | Which of the three do consultants pay for first? |

## What we are NOT building (v1)
- **Not a farmer-facing app.** Farmers buy the person, not software; direct-to-farmer fails.
- **Not hardware / a sprayer.** We're the brain on top of existing precision tools, not a robot.
- **Not the co-op enterprise product yet.** Co-ops have budget but a structural "sell less"
  conflict and slow approval — that's expansion, not the beachhead.
- **Not logistics/route optimization.** Real pain for large operators, but a different product
  and customer; revisit after the core wedge lands.
- **Not biological/genetic discovery.** Generational, but needs a science co-founder and capital.
- **Not manual data entry of records.** If it needs typing, it dies. Auto-ingest or nothing.

## Riskiest assumption
**That a willing, well-funded buyer exists who will pay enough for software whose explicit
value is using less chemical.** The most aligned buyer (independent consultant) has the
smallest budget; the best-funded buyer (co-op) has the strongest reason to block it.

**Why it is risky:** A real, painful problem does not guarantee a payer. Both the synthesis
and the synthetic panel independently landed on this as the kill-risk.
**What it would mean if wrong:** Enthusiastic users, no scalable revenue — no business, even
with a great product. Everything downstream (build, raise) would be wasted.

## Prototype success criteria
The prototype succeeds if: a real independent consultant runs it against their own fields,
the resistance recommendation is one they'd actually sign their name to, AND they commit to a
**paid pilot** for next season. (Behavior + dollars, not praise.)
The prototype fails if: consultants find the recommendation untrustworthy or unexplainable,
the data won't ingest without heavy manual entry, or they like it but won't pay a pilot fee.

## Open questions before building
- [ ] What will an independent consultant actually pay (per seat vs per acre), and will they
      commit a pilot fee? (Run the buyer-discovery guide first.)
- [ ] Can as-applied/field data be auto-ingested from the tools they already use?
- [ ] Is the wedge resistance decisioning, logistics, or knowledge capture? (Panel split 3 ways.)
- [ ] How many reachable independent consultants exist, and how do you sell to them at low cost?
