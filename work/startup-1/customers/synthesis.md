# Customer Discovery Synthesis
*Generated: 2026-06-14 | Interviews analyzed: 2*

## TL;DR

Two interviews, one clear pattern: the pain is in data gathering, not report writing.
Founders spend 90-120 minutes gathering metrics from 4+ sources before writing a
30-minute investor update. The core product challenge is trust: founders will not
send AI-gathered numbers to investors without verifying. The must-have feature is
auditability — the ability to trace every number back to its source. Two interviews
is too few to draw strong conclusions; the trust question should be explicitly
probed in the next 5 conversations.

---

## Patterns (appeared in 2+ interviews)

### Pattern 1: Data gathering dominates the time, not writing
**Frequency:** 2/2 interviews
**The problem:** In both interviews, the person described spending 2-4x more time
gathering data than actually writing. The writing is the valuable part. The gathering
is mechanical and dreaded.
**What they do today:** Manual. Pull each source separately. Paste into a doc. Check
every number before using it.
**Best quote:** "The writing I actually like. It forces me to think. The gathering
is just tedious." — Interview #1

### Pattern 2: The format never changes
**Frequency:** 2/2 interviews
**The problem:** Both interviewees use the same format for months or years. The
recipient expects the same structure. This means the gathering is highly predictable
— same sources, same fields, same format every time.
**What they do today:** Template-based. Same Google Doc or slide deck, updated in place.
**Best quote:** "I've been using the same format for 18 months. My investors actually
get annoyed if I change it." — Interview #1

### Pattern 3: Trust is the core barrier to automation
**Frequency:** 2/2 interviews
**The problem:** Both interviewees described previous automation attempts that failed.
The failure mode was not technical — it was trust. A wrong number in a report sent to
executives or investors is a professional risk.
**What they do today:** Continue to manually verify even when tools exist. "I spend more
time fixing the automation than doing it manually."
**Best quote:** "If it actually worked and I trusted the numbers" — Interview #1
(conditional phrasing is key — they want this, but they do not yet trust it)

---

## Jobs to be done

- When I sit down to send my investor update, I want to have the right numbers
  immediately, so I can spend my time writing and thinking, not gathering and checking.

- When I put a metric in a document that goes to investors or leadership, I want to
  know where it came from and that it is current, so I can send it without
  second-guessing myself.

---

## Surprises

- **The trust issue is about professional identity, not just accuracy.** Interview #2
  said: "If I'm presenting wrong numbers, what's my job?" The fear is not an error
  — it is what an error means about them. This shapes the product requirement:
  auditability is not just a nice feature, it is tied to professional identity.

- **The word "auditable" came up unprompted.** Interview #2 used this word before
  I introduced it. This means the concept is already in their vocabulary. They have
  already thought about what they would need.

- **Community exists.** Both interviewees mentioned groups of other founders or
  finance leaders who share this pain. "We commiserate about investor updates all
  the time." Word-of-mouth may be the distribution path.

---

## Key quotes (verbatim)

> "I spend more time fixing the automation than I would just doing it manually." — Interview #1

> "If it actually worked and I trusted the numbers? Honestly, yes." — Interview #1

> "I should be able to click on the MRR number and see where it came from." — Interview #2

> "Right now I'm spending 80% of my time on data plumbing and 20% on 'what does this mean.'" — Interview #2

> "The writing I actually like. It forces me to think." — Interview #1

---

## The riskiest assumption

**The product should NOT write the update — only gather the data.**

Most automations in this space try to write the narrative. Both interviewees said
they want to write the narrative themselves. If the product writes the update, it
solves the wrong problem and may not be trusted.

**Why it is risky:** It is tempting to build an AI that writes the update, because
that is the "interesting" AI feature. But that may be solving a problem that does
not exist (founders want to write).

**How to test it:** Ask the next 5 interviewees: "If the gathering was automated,
would you want the writing automated too, or would you still want to write it yourself?"

---

## What you still do not know

- [ ] What would it take for a founder to trust an automated number without checking? (probe in 5 more interviews)
- [ ] Is the trust threshold different for investor updates vs. internal reports?
- [ ] Who else in the workflow cares about the numbers — is it just the founder, or do investors push back?
- [ ] Do founders want to write the update, or is that just an artifact of not having an alternative?
- [ ] Is the pain specific to seed-stage, or does it persist at Series A/B with dedicated finance teams?

## Recommended next interviews

Talk to 5 more founders specifically about the trust question. Use this framing:
"Imagine a tool that gathered your data automatically and presented you the numbers
with a source link for each one. At what point would you send those numbers to
investors without double-checking them?" The answer will define the product requirement.
