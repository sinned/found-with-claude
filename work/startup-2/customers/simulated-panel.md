# Synthetic Customer Panel
*Generated: 2026-06-14 | Concept tested: AgroGuard — resistance-aware decision & memory layer for agronomists*

> ⚠️ **SIMULATION — a thinking tool, not research.** Every reaction below is generated, not
> collected. The panel is useful for surfacing *objection hypotheses* and finding the likely
> early-adopter segment — NOT for estimating willingness to pay, predicting adoption, or
> validating demand. See `docs/using-simulation-responsibly.md`. Take the questions to real
> people; the buyer-discovery guide in this folder is built for exactly that.

## The concept being tested
AgroGuard is software for crop advisers (not farmers). It auto-ingests as-applied spray data
and field history with no manual entry, keeps a field-by-field resistance map, and warns the
agronomist *before* each pass when a program is stacking modes of action — with an
explainable recommendation they can edit and sign. Sold per-seat to independent consultants
and as an enterprise tool to co-ops, positioned as "keep your chemistries working longer."

---

## Panel results

### Archetype 1: Aligned Independent (CCA, fee-for-service)
*Independent crop consultant | ~60,000 ac under advisement | incentive perfectly aligned, small budget*

**First reaction:**
"Finally, someone building for *me*. This is the thing I'm doing in spreadsheets and my head."

**Biggest objection:**
Price and trust in the recommendation. Her name and liability go on every rec — if she can't
see the reasoning, she won't sign it, and she can't afford much per year.

**Their question before trying it:**
"Where does the as-applied data actually come from, and can I see exactly *why* it's telling
me to switch modes of action — or am I just trusting a black box with my reputation?"

**Likelihood to try (1-5):** 5 — Acute pain, perfect fit, but converting "try" into "pay
enough to sustain a business" is the open question.

---

### Archetype 2: The Budget Owner (co-op agronomy-division manager)
*Runs agronomy for a regional co-op | controls the software budget | revenue is chemical sales*

**First reaction:**
"Interesting for continuity and defending against the independents — but you're describing a
tool that tells my growers to buy less of what I sell."

**Biggest objection:**
The business-model conflict. A "spray less" tool has to clear internal approval in a company
whose P&L is gallons sold. He needs the "chemistries last longer = long-term revenue" story to
actually hold with his board/sales side.

**Their question before trying it:**
"Does this feed our order system or fight it — and how do I explain to my sales side that I'm
paying for software that reduces volume?"

**Likelihood to try (1-5):** 3 — Has the money and a real continuity problem, but the
internal-approval friction is severe.

---

### Archetype 3: The Veteran (co-op staff agronomist, ~2 years from retirement)
*30 years territory knowledge | the "brain" the tool wants to capture | change-averse*

**First reaction:**
"I've managed this in my head for thirty years and done fine. Now I've got to feed a computer?"

**Biggest objection:**
Feels redundant or surveilled. Sees little personal upside — the knowledge-capture value
accrues to the co-op, not to him, and may feel like training his replacement.

**Their question before trying it:**
"What does this do for *me* next season — or is it just so the co-op doesn't need me?"

**Likelihood to try (1-5):** 2 — Low personal incentive; could quietly resist even if the
co-op buys it. A real adoption risk for the enterprise sale.

---

### Archetype 4: The Operator's Right Hand (large-farm manager)
*Runs spraying logistics across 9,000 ac | already has a consultant for agronomy*

**First reaction:**
"The resistance stuff my consultant already handles. Can it tell me *which fields to hit in
what order* before the weather window closes?"

**Biggest objection:**
Wrong product for him. The agronomy decisioning is solved; his pain is execution/logistics and
liability-clean records. AgroGuard as scoped doesn't address that.

**Their question before trying it:**
"Does it do logistics and audit-clean as-applied records, or is it just another agronomy
opinion I don't need?"

**Likelihood to try (1-5):** 2 — Interested in an adjacent product, not this one. Signals a
possible second wedge, not an early adopter for this scope.

---

### Archetype 5: The New Agronomist (junior co-op adviser, 2 years in)
*Covers a territory she doesn't know deeply yet | the veteran's eventual replacement*

**First reaction:**
"This would make me look ten years more experienced than I am. I'd use it every day."

**Biggest objection:**
She's not the buyer and has no authority — and worries about leaning on it so hard she never
builds her own judgment (and that growers sense it).

**Their question before trying it:**
"Will the growers trust a recommendation that's clearly coming from software and a newer face
like me?"

**Likelihood to try (1-5):** 4 — Highest *user* enthusiasm and the clearest beneficiary of
knowledge-capture, but zero buying power.

---

## Cross-panel analysis

### Where archetypes agree
- The **users** who'd benefit most (independent CCA, new agronomist) love it; the pain it
  targets is real and felt daily.
- Everyone wants **explainable** recommendations — nobody signs a black box onto their
  reputation or their grower relationship.
- Auto-ingest / no-data-entry is table stakes; the moment it needs manual entry, interest drops.

### Where archetypes diverge
| Topic | Aligned Independent | Co-op Budget Owner | Large-Farm Manager |
|-------|--------------------|--------------------|---------------------|
| Is the value real? | Yes, exactly my pain | Yes, but conflicts with my revenue | No — I need logistics, not agronomy |
| Would buy it? | Wants to, budget-limited | Can, but approval-blocked | Would buy a *different* product |
| Core driver | Decisioning + capacity | Continuity / defensibility | Execution + liability records |

### The strongest objection
**"A tool that tells my growers to buy less of what I sell has to survive approval inside a
company whose revenue is selling it."** (Co-op budget owner.)

**Why this matters:** It's not a feature gap — it's a structural conflict that sits exactly on
top of your best-funded buyer. The independents who *want* it most have the least money; the
co-ops who *have* money have the most reason to block it. This is the same risk the synthesis
flagged as the riskiest assumption, and the panel independently re-surfaced it. If this
objection isn't resolved (via positioning, pricing, or a different buyer), the product has
enthusiastic users and no scalable payer.

### Archetypes most likely to adopt early
**Independent consultants (Archetype 1)** — aligned incentive, acute pain, no internal
politics, can buy without committee. Start here even though the per-seat budget is small; they
are the cleanest path to a paying user and real proof. **New agronomists (Archetype 5)** are
the strongest *champions* inside co-ops but can't buy — useful as wedge advocates, not as the
initial sale.

## Hypotheses to test in real interviews

1. **Hypothesis:** Independent consultants will pay a real per-seat price because the tool
   lifts their acre ceiling.
   **Test with:** "What do you pay per year for software now, and what would you pay for
   something that let you take on 30% more growers without dropping quality?"

2. **Hypothesis:** Co-ops cannot approve a "spray less" tool unless it's framed as protecting
   long-term chemical revenue (stewardship), and even then approval is hard.
   **Test with:** "If a tool sometimes reduces a grower's chemical purchase this season, walk
   me through whether and how that gets approved here — and who would object."

3. **Hypothesis:** The explainability of the recommendation is a gating requirement, not a
   nice-to-have, because the agronomist's reputation/liability is on the line.
   **Test with:** "Would you put your name on a recommendation a tool generated? What exactly
   would you need to see to be comfortable doing that?"

4. **Hypothesis (adjacent):** There's a separate, possibly larger product in logistics/records
   for large operators that this scope misses.
   **Test with:** "Is your bigger pain deciding *what* to spray, or executing it across your
   acres in the window? Which would you pay for first?"

## What this panel does NOT tell you
- **Whether anyone will actually pay, or how much.** Archetype 1's "5/5 likelihood" is
  simulated enthusiasm, not a budget. Pricing must come from real buyer conversations.
- **Whether the co-op conflict is fatal or merely hard.** Only real co-op managers walking you
  through their actual approval process can tell you that.
- **Whether the three value drivers (decisioning / logistics / knowledge capture) are one
  product or three.** The panel suggests they may fracture by segment — real interviews decide.
- **Real adoption and retention.** "I'd use it every day" from a simulated persona is worth
  nothing until a real agronomist keeps opening it in week 12.
- These archetypes are partly echoes of the simulated interviews that seeded them — so the
  agreement you see is partly an artifact of my own priors, not independent confirmation.
