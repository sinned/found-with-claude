# Synthetic Customer Panel — Example Output
*Generated: 2026-06-14 | Concept: UpdateDraft — auto-pull Stripe + Mercury data with source attribution*

## The concept being tested
A tool that connects to a founder's Stripe and Mercury accounts, pulls key metrics,
and produces a pre-filled investor update template where every number shows its source
and timestamp. The founder reviews, fills in the narrative, and sends.

---

## Panel results

### Archetype 1: The Efficient Operator
*First-time founder, 18 months in, 30 investors, sends weekly updates*

**First reaction:**
"Finally. I've been looking for something like this since month 2. If the numbers are right, I'll use it."

**Biggest objection:**
"How do I know the MRR number is right? My Stripe MRR and my 'real MRR' are sometimes different because of annual contracts."

**Their question before trying it:**
"Can I see exactly which subscriptions you're counting? I need to exclude certain internal accounts."

**Likelihood to try (1-5):** 5 — Would try immediately if the source tags are granular enough.

---

### Archetype 2: The Finance-Trained Founder
*Second-time founder, prior career in consulting/finance, obsessive about accuracy*

**First reaction:**
"Interesting concept. I would not use it without seeing where every number comes from. Period."

**Biggest objection:**
"I do not put numbers in front of my investors that I haven't traced back to source. An AI summary does not constitute a source."

**Their question before trying it:**
"Can I drill down into the number? Not just see the sum — see the individual transactions that make it up?"

**Likelihood to try (1-5):** 2 — Will not adopt unless the auditability is extremely granular.

---

### Archetype 3: The Community-Connected Founder
*Active in multiple founder Slack groups, trusts peer recommendations, fast to try new tools*

**First reaction:**
"Honestly I'd try anything that fixes Sunday night. My current setup is embarrassing — I have a Google Sheet that broke twice."

**Biggest objection:**
"What if the Mercury API goes down? I've had situations where my bank connection dropped and I sent my investors wrong cash numbers."

**Their question before trying it:**
"Is there a warning if a data source is stale or couldn't connect?"

**Likelihood to try (1-5):** 5 — Would try it based on a peer recommendation alone.

---

### Archetype 4: The Pre-Traction Founder
*Raised a small pre-seed, has 8 investors, irregular update cadence, no Stripe yet*

**First reaction:**
"This is for me eventually, but not right now. I don't have Stripe set up. My main metric is users, not revenue."

**Biggest objection:**
"I'm not sure this helps pre-revenue founders. My investor updates are about user interviews and product iterations."

**Their question before trying it:**
"Can it pull from other sources — like Notion where I track user metrics — not just Stripe?"

**Likelihood to try (1-5):** 1 — Not the right timing; needs non-revenue metric support.

---

### Archetype 5: The Scaling Founder
*Series A, dedicated finance person, sends board updates not weekly investor updates*

**First reaction:**
"This sounds like what my finance person already does. Why would I use this instead of asking them?"

**Biggest objection:**
"At our stage, this should integrate with our BI tool. We have Looker. Our metrics come from there, not directly from Stripe."

**Their question before trying it:**
"Is this for seed-stage founders specifically? It doesn't sound like it's designed for Series A."

**Likelihood to try (1-5):** 1 — Wrong stage. This is not their workflow anymore.

---

## Cross-panel analysis

### Where archetypes agree
- The source attribution concept resonates — every archetype mentioned it positively or asked for more of it
- "What if the data is wrong?" is a universal concern — even the most enthusiastic archetypes asked about this
- The problem is real for archetypes 1-3; irrelevant for archetypes 4-5

### Where archetypes diverge
| Topic | Finance-trained (A2) | Community-connected (A3) |
|-------|---------------------|--------------------------|
| Trust bar | Very high — needs granular auditability | Low — peer recommendation is enough |
| First use | Will verify manually first 5+ times | Will try it immediately |
| Definition of "works" | Every number traces to individual transactions | Output looks right, feels right |

### The strongest objection
**Annual contracts and Stripe MRR calculation** — Archetype 1 identified that "Stripe MRR" and "real MRR" can diverge when annual contracts are involved. This is a legitimate edge case that, if handled poorly, would cause trust failure for the most engaged early adopters.

### Archetypes most likely to adopt early
- **Archetype 3** (Community-connected) — fastest to try, drives word-of-mouth
- **Archetype 1** (Efficient Operator) — highest retention if the source tags are granular

## Hypotheses to test in real interviews

1. **Hypothesis:** The edge case of annual contracts in Stripe MRR affects 40%+ of founders
   **Test with:** "How do you calculate your MRR? Does Stripe's MRR match your internal number?"

2. **Hypothesis:** Archetypes 4 (pre-revenue) are 20%+ of the immediate audience but not the right first target
   **Test with:** Ask next 5 interviewees if they have Stripe set up and when they started using it

3. **Hypothesis:** A "staleness warning" (data was pulled X hours ago) is a must-have for trust
   **Test with:** Show a prototype output and ask "what would make you trust or not trust this?"

## What this panel does NOT tell you
- Actual adoption rates (simulation cannot replicate real behavior)
- Whether the trust threshold is reached in practice (only real trials tell you this)
- How much founders would pay (pricing research requires real conversations with real decision-makers)
