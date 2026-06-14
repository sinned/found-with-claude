# Week 1 — Find a Problem

*Detailed account of the first week in the idea-to-Demo-Day journey.*

---

## The starting point

Sofia has spent 6 years in Revenue Operations at B2B SaaS companies. She has seen
the same workflow problems repeated at every company she has worked at. She has
2 ideas already:

1. Something to automate investor update data gathering
2. Something to make quota planning less painful

She has talked to 2 founder friends informally, but has not done structured
discovery yet. Her goal for Week 1: figure out which problem area is worth pursuing.

---

## Monday: set up the repo

Sofia cloned `founding-with-claude` and opened it in Claude Code. She dropped her
notes into `examples/founder-context.md` and `examples/messy-founder-notes.md`.

The notes were messy — two call summaries, a few random observations, and a
"what if" paragraph she had written on a walk.

---

## Monday afternoon: run the opportunity map

```
/founder-opportunity-map
```

Claude read the notes and produced a ranked opportunity memo in about 8 minutes of
conversation. Three opportunity areas were identified:

1. **Investor update data gathering** (Score: 14/15)
2. **Quota planning automation** (Score: 11/15)
3. **RevOps-to-sales handoff** (Score: 8/15)

The map revealed something Sofia had not fully articulated: her founder fit for #1
was unusually high because she had not just observed the problem — she had built
and abandoned three attempts to solve it for herself.

**The key question surfaced by the map:**
"What would it take for a founder to trust an automated number enough to send it
to investors without checking?" Sofia had not thought to ask this. She had been
thinking about the gathering problem, not the trust problem. The map reframed her
thinking.

---

## Tuesday–Thursday: validate or disprove the opportunity

Sofia did not jump to more discovery yet. The opportunity map said to "have a point
of view before talking to customers." So she spent two days stress-testing the
opportunity in her own head:

**What she mapped out:**
- Who exactly has this problem? (Seed-stage founders sending weekly updates)
- How often? (Weekly)
- What exactly are they doing today? (Manual pulling from 4-5 sources)
- Where exactly does it hurt? (Time + fear of sending wrong numbers)
- Why has no one solved this? (Trust is hard; no one has made auditability easy)

By Thursday she had a clear hypothesis: the product is not "write the investor update"
— it is "gather the data with attribution so you can trust the numbers."

---

## Friday: the weekly review

Sofia ran `/weekly-founder-review` with her notes from the week. The review produced:

**What was learned:**
- The problem is not gathering speed — it is trust in the gathered data
- Auditability (source links for every number) is likely the core product requirement
- Founder fit is unusually high because she has personally experienced the problem

**What was shipped:**
- Opportunity memo
- A clear hypothesis about what the product must do
- 5 customer conversations scheduled for next week

**The one thing for Week 2:**
Do 5 customer interviews focused specifically on the trust question, not just
the data gathering problem.

---

## What Week 1 looks like for a different founder

Week 1 is not always this clean. Common patterns:

**The founder who has too many ideas:** The opportunity map will force ranking.
Most founders discover that their #1 idea has lower founder fit than they thought.

**The founder who has no ideas yet:** The opportunity map will not work well from
nothing. Better starting question: "What work do you know better than most people?"
Start there and let the map emerge from domain expertise.

**The founder who is already committed to an idea:** The opportunity map can still
help by surfacing the assumptions behind the commitment and identifying the key
questions to answer before proceeding.

---

## Transition to Week 2

At the end of Week 1, Sofia has:
- A ranked opportunity map with clear rationale
- A specific reframe (trust > speed)
- A question to probe in every customer interview
- 5 interviews scheduled

The opportunity map did not tell her what to build. It told her what to learn next.
That is the right output for Week 1.

**Next: `journeys/week-02-customer-discovery.md`**
