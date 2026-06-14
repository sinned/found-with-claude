# Step 2 — Customer Discovery

*How to run customer discovery and synthesize it using this skill pack.*

---

## The goal

End of Step 2, you should have:
- 5-10 interviews completed
- A synthesis that identifies the core patterns
- A clear riskiest assumption to carry into Step 3

---

## The setup

Sofia came out of Step 1 with one reframe: the trust problem is more important
than the gathering problem. Every interview in Step 2 should probe this question.

Before starting Step 2 interviews, she set up:
- `examples/customer-transcript-[N].md` — one file per interview
- `.claude/skills/customer-discovery-synthesizer/templates/interview-guide.md` — 
  used to prepare for each call

---

## Monday–Thursday: 7 interviews in 4 days

Sofia aimed for 5 and got 7 by asking every interviewee for a referral at the end.

**Interview pace:** 2 per day. Back-to-back is hard — you stop really listening
by the third interview. 2 per day with reflection time between them is better.

**What she changed from Step 1:**
- She stopped pitching the product concept in the first half of the call
- She started every call: "Walk me through what Sunday evening looks like."
  (Not: "I'm building a tool for investor updates." — that primes them to tell
  her what she wants to hear.)

**The most useful question she added:**
"You've tried to automate this before. What happened?" This question, which she
did not use in Step 1, revealed the failure mode in 4 of 7 interviews: not
technical failure, but trust failure. People stopped using the automation because
they caught a wrong number once.

---

## Friday: synthesize

Sofia dropped all 7 transcripts into `examples/` and ran:
```
/customer-discovery-synthesizer
```

Claude read all 7 files, found the patterns, extracted the key quotes, and
produced the synthesis in about 10 minutes. The synthesis was immediately useful:

**What the skill found that Sofia had not noticed:**
- 3 of 7 interviewees used the word "audit" or "auditable" unprompted. Sofia had
  not noticed this pattern across interviews because she was in each one separately.
- The "format never changes" pattern appeared in 6 of 7 interviews, which confirmed
  that the automation problem was predictable — but she had only been thinking about
  2 of her own interviews when she noticed this.

**What the synthesis surfaced as the riskiest assumption:**
"Founders will send AI-gathered numbers to investors without manually verifying,
IF source attribution is shown inline."

Sofia had been thinking "the problem is trust" — the synthesis made it more specific:
trust is solvable if (and only if) the output shows its work. This is a testable assumption.

---

## The synthesis review conversation

After the synthesis, Sofia spent 15 minutes going back to Claude with follow-up questions:

- "What pattern appeared in the interviews about how founders check their numbers?"
  → Revealed that most founders have a mental model of "the number in my head" that
  they compare against the pulled number. The real check is not "is it right" but
  "does it match what I expected?"

- "Which interviewee was most skeptical about automation?"
  → Interviewee #6 (finance background) — and the reasons they gave were the most
  specific and technical of anyone interviewed.

This kind of follow-up conversation with the synthesis is more useful than re-reading
the transcripts. The synthesis is the context; the conversation is the analysis.

---

## End of week: what changed

**Starting assumption:** "The problem is data gathering."
**Ending assumption:** "The problem is trust in gathered data — specifically, trust
that requires source attribution."

This reframe affects the prototype. A prototype that gathers data without attribution
would fail the test. A prototype that gathers data with attribution might pass.

**Step 2 decision:** Proceed to `/synthetic-customer-panel` to stress-test the
concept before writing the product brief.

**Next: `journeys/week-03-customer-simulation.md`** (not yet written)
