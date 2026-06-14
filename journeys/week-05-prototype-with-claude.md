# Week 5 — Prototype with Claude

*How the prototype sprint works and how it connects to the sibling repo.*

---

## The starting point

Sofia has:
- A clear product brief from Week 4
- A specific riskiest assumption: "Founders will trust AI-gathered numbers
  with source attribution and send them to investors without double-checking"
- A 1-week time budget
- Claude Code and access to `../prototype-with-claude`

---

## Monday: scope the prototype

```
/prototype-scope
```

The scope document produced by this skill:

**The one job:** Take a seed-stage founder's Stripe and Mercury data and produce
a pre-filled investor update template with a source link for every number.

**In scope (v0):**
- Connect to Stripe API (read MRR, new revenue, churn)
- Connect to Mercury API (read current cash balance, burn rate)
- Format output as a template with [Stripe — pulled 2026-06-14 at 11pm] source tags
- Allow founder to edit before sending

**Out of scope:**
- Linear integration (API complexity, not worth it for v0)
- Writing the narrative (founders want to write it themselves)
- Email sending (out of scope — just produce the doc)

**Success criteria:**
A founder can go from "no data pulled" to "pre-filled template with source links"
in under 5 minutes, and would be willing to send those numbers to investors without
going back to check Stripe.

**Readiness checklist:** ✅ All items checked. Ready to build.

---

## Monday afternoon: open the sibling repo

Sofia opened a new terminal tab and navigated to `../prototype-with-claude`.

```bash
cd ../prototype-with-claude
claude
```

She read `WALKTHROUGH.md` to understand the eval/improve loop (15 minutes).

Then she ran:
```
/new-skill
```

Claude walked her through a wizard:
- "What is the job?" → Sofia pasted in the one-job statement from her scope doc
- "What are the inputs?" → Stripe API credentials + Mercury API credentials
- "What does success look like?" → The success criteria from the scope doc

Claude produced a draft `SKILL.md` for a skill called `generate-investor-update`.

---

## Monday–Tuesday: write and iterate on the skill

Sofia's first SKILL.md was functional but had a key gap: the output format did
not include source attribution. The skill was producing a template, but each number
appeared without its source tag.

She ran `/improve-skill generate-investor-update` and described the failure:
"The output has the numbers but not the source links. The format should say
[$12,400 MRR, from Stripe, pulled 2026-06-14] after every number."

After one improve cycle, the source attribution appeared.

First eval run: 72% (13/18 criteria). Top failures:
- Mercury API call was failing on certain account types
- Burn rate was being calculated wrong (monthly instead of daily average)

Second improve cycle fixed both. Eval score: 88%.

---

## Wednesday–Thursday: first real test

Sofia ran the skill on her own accounts. Output: a pre-filled investor update
with source links for 5 metrics. She read every number and every source tag.

Her reaction: "I would send this." 

She sent it to a friend who was a seed-stage founder: "Would you send these numbers
to your investors without going back to check?" Answer: "Yes, because I can see
where each number came from."

This was the first positive evidence for the riskiest assumption.

---

## Friday: prototype review

Sofia returned to `founding-with-claude` and ran:
```
/prototype-review
```

Input: the scope document + the eval report + the friend's reaction.

**Verdict: PROVEN — partially.** The prototype demonstrated that source attribution
enables trust for at least 2 data points (the builder and 1 external user). Not
enough users to call this validated, but enough to proceed to first-user outreach.

**What the prototype revealed:**
- The Stripe and Mercury integrations work reliably
- Source attribution is the key differentiator — founders respond to it
- Linear integration is genuinely harder than expected (confirmed the out-of-scope decision)
- The output format needs to handle the case where a founder has not set up Stripe yet

**What the prototype did NOT prove:**
- Whether 10+ founders would send without checking (2 is not enough)
- Whether the trust holds after the first few times (novelty effect possible)

---

## The handoff loop

```
Week 4: /product-strategy-brief
     ↓
Week 5a: /prototype-scope
     ↓
prototype-with-claude: /new-skill → /eval-skill → /improve-skill
     ↓
Week 5b: /prototype-review
     ↓
Week 6: /first-users-outreach
```

This loop is reusable. Every time the prototype needs to change based on user
feedback, Sofia can:
1. Scope the change in `founding-with-claude` with `/prototype-scope`
2. Implement in `prototype-with-claude` with `/improve-skill`
3. Review in `founding-with-claude` with `/prototype-review`

---

## What a prototype week looks like for a non-technical founder

The skill in `prototype-with-claude` is written in plain text (SKILL.md). A
non-technical founder can:
- Write the SKILL.md with Claude's help using `/new-skill`
- Run and iterate with Claude doing the API work
- Evaluate the output using `/eval-skill`

What they cannot do without engineering help:
- Build production-quality API integrations (auth flows, error handling, rate limits)
- Deploy as a standalone product (the skill runs in Claude Code, not in a browser)
- Handle security requirements for storing API credentials

For a pure prototype week: Claude Code is enough. For a product that founders can
sign up for: you need an engineer or a no-code deployment layer.

**Next: `journeys/week-06-first-users.md`**
