# Knowledge Store

The structured knowledge base for this startup. Grows over time as skills run.
Designed for clean export to an external durable knowledge store when ready.

---

## What this is

Every time a skill runs, it does two things:

1. Writes a **working document** to `work/[startup]/[skill]/` — the full output for
   human review. Raw, may be overwritten.

2. Extracts **knowledge entities** here — curated facts that accumulate over time.
   These are NOT summaries of the output. They are the most important things learned,
   pulled out and structured so they can inform every future skill that runs.

The `work/` files answer "what did this skill produce?"
The `knowledge/` entries answer "what do we know, and why?"

---

## The future: durable knowledge store

This directory is structured so it maps directly to an external durable knowledge
store (vector database, document store, or structured database) when ready.

When that transition happens:
- Each `knowledge/[startup]/[type]/[slug].md` → one document/record in the store
- YAML frontmatter → record metadata and fields
- Markdown body → document content
- Skill writes files → skill POSTs to the knowledge store API
- Skill reads files → skill queries the knowledge store API

**The schema does not change. Only the transport changes.**

This is the API contract: a developer implementing the external store should be
able to derive the full API from this README alone.

---

## Entity types

| Type | What it captures | Produced by |
|------|-----------------|-------------|
| `insight` | A cross-cutting learning from research or experimentation | discovery-synthesizer, panel, pmf-review |
| `problem` | A specific pain point with evidence and severity | opportunity-map, discovery-synthesizer |
| `customer` | A segment or archetype: who they are, what they need, how to reach them | discovery-synthesizer, panel |
| `assumption` | A hypothesis, tracked through validation or invalidation | strategy-brief, prototype-scope, opportunity-map |
| `decision` | A product or strategy choice with the reasoning and alternatives | strategy-brief, weekly-review |
| `signal` | A PMF or market signal with strength and evidence | pmf-review, weekly-review |
| `experiment` | A growth experiment: hypothesis, method, result | growth-experiment-backlog |
| `person` | An individual contact (interviewee, early user, advisor) | discovery-synthesizer, outreach |

---

## Schema

Every knowledge entity is a markdown file with YAML frontmatter:

```yaml
---
id: kebab-case-slug-matching-filename
type: insight | problem | customer | assumption | decision | signal | experiment | person
source: skill-name-that-produced-this
created: YYYY-MM-DD
startup: startup-N
confidence: high | medium | low
status: active | superseded | invalidated
tags:
  - tag-1
  - tag-2
---
```

### Body formats by type

**`insight`**
```markdown
# [What was learned, as a declarative statement]

[2-3 sentences explaining the insight and its significance]

**Evidence:** [Specific data points, quotes, or interview count that support this]
**Implication for product:** [What this means for what to build]
**Open question:** [What this still does not tell you]
```

**`problem`**
```markdown
# [Problem stated as: people who do X suffer from Y]

[Description of the problem and why it is hard to solve]

**Who has it:** [Specific customer context — role, stage, situation]
**Severity:** [Time/money/frustration cost — be specific]
**Current workarounds:** [What people actually do today]
**Evidence:** [Interview count, quotes, or observed behavior]
```

**`customer`**
```markdown
# [Segment name — specific, not generic]

[Who this is: role, company stage, context in which they experience the problem]

**Job to be done:** When [situation], I want to [motivation], so I can [outcome].
**How they describe the pain:** "[In their own words or close paraphrase]"
**What they currently use:** [Existing tools or workarounds]
**Why they'd switch:** [What would have to be true for them to change]
**Evidence:** [Interview count, representative quotes]
```

**`assumption`**
```markdown
# [The assumption, stated as a falsifiable claim]

**Validation status:** unvalidated | validated | invalidated
[Why we believe this is true — or believed it when we wrote it]

**What "validated" looks like:** [Specific observable evidence]
**What "invalidated" looks like:** [What would prove this wrong]
**How we'll test it:** [The experiment or research approach]
**Current evidence:** [What we know so far — possibly empty]
```

**`decision`**
```markdown
# [The decision, stated as a choice that was made]

**Made:** [date]
**Status:** active | revisited | reversed

[Why we made this decision]

**Alternatives considered:** [What else we looked at and why we rejected it]
**What would cause us to revisit this:** [The condition that would change our mind]
```

**`signal`**
```markdown
# [The signal — what was observed]

**Type:** retention | engagement | referral | willingness-to-pay | usage | other
**Strength:** strong | moderate | weak | neutral

[Description of what was observed and what it means]

**Evidence:** [Specific data: numbers, quotes, dates]
**Interpretation:** [What this tells us about PMF]
**Confidence:** [How sure we are — and why we might be wrong]
```

**`experiment`**
```markdown
# [Experiment name]

**Status:** planned | running | complete
**Hypothesis:** [If we do X, we expect Y because Z]
**Method:** [What we actually did]
**Result:** [What happened — be honest]
**Learning:** [What this tells us — positive or negative]
```

**`person`**
```markdown
# [Name or pseudonym]

**Role:** [Their job/context]
**Relationship:** interviewee | early-user | advisor | investor | other

[Key things learned from or about this person]

**Best quote:** "[verbatim or near-verbatim]"
**Follow-up:** [Any open loop with this person]
```

---

## Directory structure

```
knowledge/
  README.md                 ← this file (schema spec + future API contract)
  startup-1/
    insights/               ← [slug].md for each cross-cutting learning
    problems/               ← [slug].md for each pain point
    customers/              ← [slug].md for each segment or archetype
    assumptions/            ← [slug].md for each tracked hypothesis
    decisions/              ← [slug].md for each strategy/product decision
    signals/                ← [slug].md for each PMF signal
    experiments/            ← [slug].md for each growth experiment
    people/                 ← [slug].md for each individual contact
  startup-2/
    ...
```

---

## What skills write here (and what they don't)

**Write a knowledge entity when:**
- A pattern appeared in 2+ interviews (→ `insight`)
- A specific pain point is identified with evidence (→ `problem`)
- A customer segment is defined with enough detail to build from (→ `customer`)
- An assumption is made explicit (→ `assumption`)
- A product or strategy decision is made and should be remembered (→ `decision`)
- A PMF signal is observed (→ `signal`)
- A growth experiment completes (→ `experiment`)

**Do not write here:**
- Vague or generic claims ("customers want a better product" is not an insight)
- Full summaries of output documents (that is what `work/` is for)
- Things that are immediate next steps or tasks (track those in conversation)
- Anything that will be overwritten on the next skill run

---

## How later skills read from here

When a skill needs context from prior runs, it reads from `knowledge/[startup]/[type]/`.
This is especially useful for:

- `/synthetic-customer-panel` → `knowledge/[startup]/customers/` for realistic archetypes
- `/product-strategy-brief` → `knowledge/[startup]/assumptions/` for what's unvalidated
- `/fundraising-narrative` → `knowledge/[startup]/signals/` and `decisions/`
- `/weekly-founder-review` → all types, for a complete weekly picture
- `/loop` → `knowledge/[startup]/assumptions/` to check what's still unvalidated
