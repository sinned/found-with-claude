# Prototype with Claude: The Build Phase of the Founder Journey

*A positioning piece explaining how the sibling repo fits into the founding journey*

---

Week 5 is prototype week.

You have done the interviews. You have the synthesis. You have a product brief with
a riskiest assumption. You know what you need to build and what you are trying to prove.

Now you need to build it in a week.

This is where `prototype-with-claude` comes in.

---

## What prototype-with-claude is

`prototype-with-claude` is a build environment for AI feature prototyping. It
teaches a specific workflow:

```
Write a SKILL.md (plain-text job description)
→ Run it in Claude Code (Claude executes it immediately)
→ Measure quality with evals (Claude grades its own outputs)
→ Improve automatically (/improve-skill edits the SKILL.md)
→ Ship to production (/export-to-sdk generates Python)
```

The core insight: most AI feature prototyping fails because founders write SDK code
before they know what the agent should actually do. Writing SDK code is expensive
to iterate on — every change requires redeployment. Skills fix that. A SKILL.md
takes 10 minutes to write and 30 seconds to test.

---

## Why the order matters

In the founding journey, the prototype sprint comes after:
1. Knowing the specific problem
2. Knowing the specific customer
3. Having a clear product brief with a riskiest assumption
4. Running `/prototype-scope` to define what to build

Without that foundation, the prototype sprint produces the wrong thing. You build
something technically impressive that does not test the riskiest assumption. You
spend a week building confidence in a bet you have not actually made.

`/prototype-scope` (in this repo) produces the document that gates the sprint.
The document defines: the one job, the inputs, the outputs, the success criteria,
and what is explicitly out of scope. Only then does the founder open `prototype-with-claude`.

---

## What happens in the sprint

**Day 1:** Open `prototype-with-claude`. Run `/new-skill`. Claude guides you through
creating a SKILL.md from your scope document. First test run by end of day.

**Day 2-3:** Iterate. Run `/eval-skill` to see where the skill fails. Run
`/improve-skill` to fix the failures automatically. Most skills go from 65% to 85%
eval score in 2-3 cycles.

**Day 4:** First real test with real data. Not test cases — the actual thing. Does
it produce output the founder would trust?

**Day 5:** If the test passes, show it to 1-2 target users live. Their reaction
is the signal. Return to `founding-with-claude` and run `/prototype-review`.

---

## The three skill patterns in prototype-with-claude

The repo teaches three shapes for AI features:

**Research & Synthesize:** Search → gather → synthesize → structured output.
Use for: customer research, competitor analysis, market briefs, deal diligence.
Built-in example: `/research-agent <topic>`

**Score & Classify:** Load rubric → analyze → score → decision.
Use for: lead qualification, support triage, content moderation, prioritization.
Built-in example: `/qualify-lead <company>`

**Generate & Iterate:** Brief → research → 3 variations → recommendation.
Use for: content generation, outreach drafts, proposal writing.
Built-in example: `/generate-content "<brief>"`

Most startup AI features fit one of these three shapes.

---

## When to use it and when to skip it

**Use prototype-with-claude when:**
- You are building an AI-powered feature (an agent that does a job)
- You need to validate the AI behavior before writing production code
- You want to show a founder how to build fast without boilerplate

**Skip prototype-with-claude when:**
- Your prototype is a static mockup (use Figma or HTML)
- Your prototype is a database operation (no AI needed)
- Your prototype requires a real production backend (different workflow)

The skill in `prototype-with-claude` is what gets you from "I know what the
agent should do" to "I have a working demo" in 1-5 days without writing production
code. It is the right tool for Week 5.

---

## The connection back to this repo

After the prototype sprint, the founder returns to `founding-with-claude` and runs
`/prototype-review`. This is the evaluation of what was built against the original
strategy.

The review asks: did the prototype test the riskiest assumption? Did it meet the
success criteria from the scope document? And — most importantly — what do we do next?

The answer drives the rest of the journey: get first users, measure PMF signals,
grow, hire, fundraise.

The prototype is not the destination. It is the evidence that the destination exists.
