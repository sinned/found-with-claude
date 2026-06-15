---
name: demo-day-script
description: Write a 2-minute Demo Day pitch script with hook, problem, solution, traction, and ask. Produces a word-for-word script and timing guide. Use when preparing for Demo Day, investor pitch, or any high-stakes short pitch. Trigger phrases: "demo day script", "write my pitch", "2-minute pitch", "YC demo day", "investor presentation script".
---

# Demo Day Script

Takes the fundraising narrative and produces a 2-minute Demo Day script — every
word, timed, with transitions. No bullet points. No "and then we." A script you
can say aloud.

## Input

Look for:
- `work/fundraising-narrative/fundraising-narrative-output.md` — the full narrative
- `work/pmf-signal-review/pmf-signal-review-output.md` — the traction numbers
- Any specific Demo Day format the founder mentions (YC is 2 minutes, others vary)
- Whether there is a live demo in the middle (changes the pacing)

If no fundraising narrative exists: run `/fundraising-narrative` first. A Demo Day
script without a narrative is just words.

## Steps

1. **Extract the five elements** from the narrative:
   - **Hook** — the one sentence that makes investors lean in
   - **Problem** — who suffers, how much, what they do today
   - **Solution** — what you built and the key insight
   - **Traction** — the number that proves it is working
   - **Ask** — how much, to do what

2. **Time the elements** — Standard YC split (2 minutes = ~300 words at natural pace):
   - Hook: 10-15 seconds
   - Problem: 20-25 seconds
   - Solution: 30-40 seconds
   - Traction: 15-20 seconds
   - Ask + team: 15-20 seconds
   - (Live demo if included: 30-40 seconds, displaces some solution time)

3. **Write the hook first** — The hook determines whether investors listen to the
   rest. Write 5 hook options. Pick the sharpest one.

4. **Write the full script** — Word for word. Every transition. No bullet points.
   The script should sound like a person talking, not a presentation being read.

5. **Add timing markers** — Show the founder when they should be at each beat.

6. **Identify the danger zones** — Where founders typically go too long or lose
   the audience.

7. **Write the script** — Follow the output format below.

8. **Save output** — Write to `work/demo-day-script/demo-day-script-output.md`.

## Output format

```markdown
# Demo Day Script
*Generated: [date] | Total time: 2:00 | Format: [no demo / live demo]*

---

## Hook options (pick one)

Option A (problem-first): "[Hook — one sentence that makes investors feel the pain]"
Option B (traction-first): "[Hook — lead with the most impressive number]"
Option C (insight-first): "[Hook — lead with the non-obvious thing you know]"

**Recommended:** Option [X] because [why this one works best for this company]

---

## Full script

[0:00]
"[Hook sentence — make it land. Period.]

[0:10]
[Problem — specific person, specific situation, specific pain. Present tense.
'Every [customer] spends [time/money] doing [thing] because [root cause].']

[0:30]
[Solution — what you built in one sentence. Then the key insight.
'We built [product] that [does X]. The key insight is [non-obvious thing].'
If live demo: '[transition to demo]' — keep it tight, 30 seconds max]

[1:10]
[Traction — the number that proves it is working.
'[N] [customers/users/companies] are [using/paying/doing] with [key signal].'
Include growth rate if strong: 'Growing [X]% week-over-week.']

[1:30]
[Why us — one sentence. Not credentials. What you have done.
'We are the team that [specific proof of capability].']

[1:40]
[Ask — amount, use of funds, milestone.
'We are raising $[X] to [specific thing you will build or prove].
At the end of this round, we will have [specific milestone].']

[1:55]
'[Company name]. [One-sentence company description.]
[Website or contact].'

[2:00]"

---

## Timing guide

| Beat | Target time | Warning time |
|------|-------------|--------------|
| Hook | 0:10 | 0:15 |
| Problem | 0:30 | 0:40 |
| Solution | 1:10 | 1:20 |
| Traction | 1:30 | 1:40 |
| Ask | 1:50 | 1:58 |
| Close | 2:00 | 2:05 |

## Danger zones

- **Problem section:** Most founders go too long. If you have not gotten to solution
  by 0:35, you are over.
- **Solution section:** Most founders explain how, not what. Investors want to know
  what it does, not how it works. Technical explanation kills the pitch.
- **Traction section:** Most founders understate or oversell. Say the number flat.
  Let the number do the work.
- **Ask section:** Most founders get vague. "We are raising capital to grow the team"
  is not a use of funds. "[N] engineers + [N] months to hit [specific milestone]" is.

## Practice instructions

1. Read the script aloud 3 times before any other feedback
2. Record yourself on video once — watch it once
3. Practice the transitions: hook → problem, problem → solution
4. Practice the ask last — it is usually where the momentum dies
5. Time yourself without a timer. If you feel rushed, the script is too long.
6. The goal: deliver it at 80% energy in rehearsal so 100% on stage feels natural
```

## What makes a great Demo Day pitch vs. a fine one

**Fine:** A clear explanation of what you do and your traction.

**Great:** Investors feel the problem, believe you are the team, and want to talk
to you after.

The difference is usually in the hook and the one sentence that explains the insight.
Spend 80% of your preparation time on those two things.

## What a hook is NOT

- "We are building the future of X" — meaningless
- "Every company needs Y" — too generic
- "We are at the intersection of A and B" — consultant speak

What a hook IS:
- "Last year, [specific person] spent $50,000 paying consultants to do [thing]
  that our software does in 4 minutes."
- "3 of us built this because we spent 6 months trying to solve this problem for
  ourselves and failed with every existing tool."
- "We have [N] paying customers and we have not launched yet."
