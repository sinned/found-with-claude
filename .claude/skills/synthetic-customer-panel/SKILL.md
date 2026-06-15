---
name: synthetic-customer-panel
description: Simulate reactions from distinct customer archetypes to a product concept, feature idea, or pricing model. Use when a founder wants to stress-test an idea before building or before the next round of customer interviews. IMPORTANT: This is a thinking tool, not a research substitute. See docs/using-simulation-responsibly.md. Trigger phrases: "simulate customer reactions", "run a synthetic panel", "what would customers think of this", "stress-test this idea".
---

# Synthetic Customer Panel

Simulates reactions from 4-6 distinct customer archetypes to a product concept,
feature idea, or pricing model. Surfaces objections, edge cases, and questions
that the founder may not have considered.

**Important:** This is a thinking tool, not a research substitute. Read
`docs/using-simulation-responsibly.md` before drawing conclusions from panel output.

## Input

The founder needs to provide:
1. **A concept to test** — A product idea, feature, pricing model, or positioning
2. **Customer context** (use one of these sources):
   - Output from `/customer-discovery-synthesizer` in `work/[startup]/customer-discovery-synthesizer/customer-synthesis-output.md`
   - A description of the target customer in the current conversation
   - `work/[startup]/founder-opportunity-map/founder-context.md`

If the founder has not provided a clear concept, ask: "What exactly do you want to
test? Describe it in 2-3 sentences as you would to a customer."

## Steps

1. **Define the archetypes** — Based on the customer context, identify 4-6 distinct
   customer archetypes. Each archetype should differ meaningfully on at least two
   dimensions (e.g., company size, role, sophistication, current workflow).
   Name each archetype descriptively.

2. **Describe each archetype** — For each: role, company context, current workflow,
   what they care most about, what they are skeptical of. Be specific.

3. **Simulate the first reaction** — For each archetype, write their immediate
   reaction to hearing the concept described in 1-2 sentences. First impressions,
   before they ask questions.

4. **Simulate the objections** — For each archetype, what is their biggest concern?
   What would make them say no? What are they afraid of?

5. **Simulate the questions** — What would each archetype ask before agreeing to try it?

6. **Identify the strongest objection overall** — Which objection, if unresolved,
   would kill this product for the largest number of people?

7. **Generate hypotheses to test** — Turn the top 3 objections into specific
   interview questions or experiments.

8. **Write the panel report** — Follow the output format below.

9. **Save output** — Write to `work/[startup]/synthetic-customer-panel/synthetic-customer-panel-output.md`.

## Output format

```markdown
# Synthetic Customer Panel
*Generated: [date] | Concept tested: [name]*

## The concept being tested
[2-3 sentence description of the concept as presented to the panel]

---

## Panel results

### Archetype 1: [Name]
*[Role] at [company type] | [Size/stage] | [Key characteristic]*

**First reaction:**
[1-2 sentences — immediate gut response]

**Biggest objection:**
[Their core concern — be specific]

**Their question before trying it:**
"[Verbatim-style question they would ask]"

**Likelihood to try (1-5):** [X] — [One sentence explanation]

---

### Archetype 2: [Name]
[Same structure...]

---

## Cross-panel analysis

### Where archetypes agree
- [Point of consensus — what most archetypes said similarly]

### Where archetypes diverge
| Topic | [Archetype A] | [Archetype B] |
|-------|---------------|---------------|
| [Topic] | [View] | [View] |

### The strongest objection
[The objection that, if unresolved, would kill the product for the most people]

**Why this matters:** [Why this is not just a concern but a possible product killer]

### Archetypes most likely to adopt early
[Which 1-2 archetypes would adopt this first and why]

## Hypotheses to test in real interviews

1. **Hypothesis:** [What the panel suggests might be true]
   **Test with:** "[Specific question to ask a real customer]"

2. [Another hypothesis...]

## What this panel does NOT tell you
[Be specific about what simulation cannot reveal for this particular concept]
```

## Calibration note

The synthetic panel is most useful for:
- Generating objection hypotheses (not validating them)
- Finding the customer segment most likely to adopt early
- Preparing for real customer conversations

It is least useful for:
- Estimating willingness to pay (real pricing research requires real conversations)
- Predicting adoption rates (simulation cannot replicate actual behavior)
- Validating demand (only real users can do that)

Always end the session by recommending which real customers to talk to next based
on what the panel revealed.
