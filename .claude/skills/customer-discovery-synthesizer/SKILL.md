---
name: customer-discovery-synthesizer
description: Synthesize raw customer interview notes or transcripts into structured insight. Use when a founder has done customer discovery interviews and wants to find patterns, extract jobs-to-be-done, and identify what to build. Trigger phrases: "synthesize my interviews", "analyze my customer calls", "what did I learn from customers", "pull out patterns from these transcripts".
---

# Customer Discovery Synthesizer

Takes raw interview notes, transcripts, or voice memo summaries and produces a
structured synthesis — identifying patterns, extracting jobs-to-be-done, surfacing
the most important quotes, and flagging what is still unknown.

## Input

Look for interview material in:
- Files mentioned in the current conversation
- `work/customer-discovery-synthesizer/customer-transcript-*.md` — individual transcripts
- `work/founder-opportunity-map/messy-founder-notes.md` — raw notes from calls
- Any other files the founder points to

Accept any format: structured Q&A, stream-of-consciousness notes, bullet lists,
full transcripts. The skill works from messy input.

If only 1-2 transcripts are available: synthesize them but note that the sample
is too small to draw confident conclusions. Identify the next questions to ask.

If 5+ transcripts are available: look for convergence across interviews.

## Steps

1. **Read all available interview material.** Do not summarize prematurely —
   read everything before forming conclusions.

2. **Extract raw signals** — From each interview, pull out:
   - The specific problem the person described (in their words)
   - What they currently do to solve it (workarounds, tools, manual work)
   - How much it costs them (time, money, frustration)
   - What they said that surprised you
   - Any direct quotes worth preserving verbatim

3. **Find patterns across interviews:**
   - What problem came up in 3+ interviews?
   - What workaround came up in 3+ interviews?
   - What surprised you in 2+ interviews?
   - What do interviewees disagree about?

4. **Identify jobs-to-be-done** — What are people actually trying to accomplish?
   Frame each job as: "When [situation], I want to [motivation], so I can [outcome]."
   This is different from the problem they described. It is the underlying goal.

5. **Identify the riskiest assumption** — Based on what you heard, what is the
   one thing that must be true for this product to succeed that is NOT yet confirmed?

6. **Flag open questions** — What do you still not know? What would you ask in the
   next 5 interviews?

7. **Write the synthesis** — Follow the output format below.

8. **Save output** — Write to `work/customer-discovery-synthesizer/customer-synthesis-output.md`.

## Output format

```markdown
# Customer Discovery Synthesis
*Generated: [date] | Interviews analyzed: [N]*

## TL;DR
[3-4 sentences: what you heard, what it means, what to do next]

## Patterns (appeared in 3+ interviews)

### Pattern 1: [Name]
**Frequency:** [N/N interviews]
**The problem:** [What they described, in plain language]
**What they do today:** [Current workarounds]
**Best quote:** "[verbatim quote from interview that captures this best]"

### Pattern 2: [Name]
[Same structure...]

## Jobs to be done

- When [situation], I want to [motivation], so I can [outcome].
- [Another JTBD...]

## Surprises (things you did not expect to hear)

- [Surprise 1 — what was said, why it surprised you]
- [Surprise 2...]

## Disagreements (interviewees who said different things)

| Topic | Position A | Position B | Who held each |
|-------|------------|------------|---------------|
| [Topic] | [View] | [View] | [Interviews] |

## Key quotes (verbatim, worth preserving)

> "[Quote 1]" — [Interviewee descriptor, e.g., "Series A founder, 8 employees"]

> "[Quote 2]" — [Descriptor]

## The riskiest assumption

[One sentence: the thing that must be true for this product to work that is NOT
yet confirmed by what you heard]

**Why it is risky:** [Why this might not be true]
**How to test it:** [Specific experiment or next interview question]

## What you still do not know

- [ ] [Open question 1 — specific, testable]
- [ ] [Open question 2...]

## Recommended next interviews

[Who to talk to next, and what specific question to prioritize]
```

## If interviews are very messy or incomplete

- If a "transcript" is just 5 bullet points: extract what you can, note what is missing
- If quotes are paraphrased rather than verbatim: use them but label as "paraphrase"
- If only 1-2 people were interviewed: synthesize them, but open with: "This is based on
  [N] interviews — not enough for confident conclusions. Treat this as hypotheses to test."

## What makes a good synthesis vs. a bad one

**Bad synthesis:** "Customers want a better solution." (too vague)
**Good synthesis:** "3/7 founders said they spend 3+ hours pulling together data
  from Stripe, Linear, and bank accounts before writing their weekly investor update."

Always prefer specific over general. Always prefer quotes over paraphrases.
Always surface what you still do not know.
