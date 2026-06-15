---
name: founder-hiring-scorecard
description: Create a structured hiring scorecard for an early-stage startup role. Produces must-haves, nice-to-haves, red flags, and interview questions calibrated to the specific role and stage. Use when a founder is about to hire. Trigger phrases: "hiring scorecard", "help me hire", "what should I look for in", "interview questions for", "first hire criteria".
---

# Founder Hiring Scorecard

Produces a structured hiring scorecard for an early-stage role: what you must have,
what is nice to have, what the red flags are, and specific interview questions to
find out which column a candidate belongs in.

## Input

The founder needs to provide:
- The role they are hiring for (title and what the person will actually do)
- The current team context (who is already there, what is already covered)
- The company stage and the single biggest problem this hire should solve

Ask if missing: "What is the one thing you most need this person to do in the
first 90 days that no one on the current team can do?"

## Steps

1. **Clarify the actual job** — What will this person do on day 1, week 1, month 3?
   Most early-stage job descriptions describe a fantasy. The scorecard should
   describe the actual job.

2. **Define the must-haves** — 3-5 things that, if absent, would disqualify a
   candidate regardless of everything else. Must-haves should be observable, not
   abstract. Not "strong communication skills" — "has written clearly under pressure
   before, with examples."

3. **Define the nice-to-haves** — 3-5 things that would make a candidate better
   but are not disqualifying. These are the things you would teach a great person.

4. **Define the red flags** — 3-5 things that would make you doubt a candidate
   even if everything else seemed right. Red flags for early-stage hires are often
   different from later-stage hires.

5. **Write the interview questions** — 6-8 questions that actually reveal which
   column a candidate belongs in. No hypothetical questions ("What would you do
   if..."). Only behavioral questions ("Tell me about a time when...") and work
   samples ("Here is a real problem we are working on. How would you approach it?").

6. **Define the work sample** — One specific exercise that reveals whether the
   person can actually do the job. This is more valuable than any interview question.

7. **Write the scorecard** — Follow the output format below.

8. **Save output** — Write to `work/[startup]/founder-hiring-scorecard/hiring-scorecard-[role].md`.

## Output format

```markdown
# Hiring Scorecard: [Role Title]
*Generated: [date] | Stage: [company stage] | Priority: [what this hire unlocks]*

## The actual job (first 90 days)

- Month 1: [What they will actually do — specific, not abstract]
- Month 2: [How the job evolves]
- Month 3: [What success looks like — specific, measurable]

## Must-haves (disqualify if absent)

| Must-have | How to assess |
|-----------|--------------|
| [Must-have 1 — specific and observable] | [What to look for / what question to ask] |
| [Must-have 2] | |
| [Must-have 3] | |

## Nice-to-haves (would be great but not disqualifying)

- [Nice-to-have 1]
- [Nice-to-have 2]
- [Nice-to-have 3]

## Red flags (cause to doubt even if everything else seems right)

- [Red flag 1 — specific to early-stage, not generic]
- [Red flag 2]
- [Red flag 3]

## Interview questions

**On the core job:**
1. "[Question about specific situation where they did the core job]"
   *Listen for: [What a strong answer sounds like]*

2. "[Question about a failure or challenge in this domain]"
   *Listen for: [Self-awareness, learning, specific detail]*

**On early-stage fit:**
3. "[Question about working in ambiguity]"
   *Listen for: [Examples of building something from scratch]*

4. "[Question about working without resources]"
   *Listen for: [Resourcefulness, not complaints about lack of support]*

**On culture and judgment:**
5. "[Question that reveals values]"
   *Listen for: [Specific behavior, not aspirational statements]*

6. "[Question about a disagreement or conflict]"
   *Listen for: [Directness, resolution, learning]*

## The work sample

**Assignment:** [1-2 sentence description of a real problem to solve]

**Time:** [X hours — keep it short, under 3 hours]

**What you are evaluating:** [The 3 specific things you will look at]

**What strong looks like:** [Concretely]
**What weak looks like:** [Concretely]

## Scoring guide

After each interview, score the candidate:

| Dimension | 1 (weak) | 3 (meets bar) | 5 (exceptional) | Your score |
|-----------|----------|---------------|-----------------|------------|
| Core job capability | | | | /5 |
| Early-stage fit | | | | /5 |
| Judgment | | | | /5 |
| [Role-specific] | | | | /5 |

**Recommend to hire if:** Total ≥ 16/20 AND no must-have gaps
**Pass if:** Total < 14/20 OR any must-have gap
**Discuss if:** Total 14-15/20 AND no must-have gaps
```

## Early-stage red flags worth calling out

These are common early-stage hiring mistakes:

- **"I need to build a team before I can do X"** — Early employees build, they do not manage
- **Asks about equity without asking about the mission** — Incentive misalignment
- **Has only worked in large orgs** — May not thrive without structure (not a disqualifier, but probe it)
- **Describes a role, not a job** — Says what their title was, not what they built
- **Cannot describe a single failure in detail** — Either inexperienced or not self-aware

## The most common early hiring mistake

Hiring for the company you hope to be, not the company you are. The best person
to be your first sales hire is often not someone with "VP Sales" on their resume
— it is someone who loves selling and is willing to make 50 cold calls a week.

Write the scorecard for the company you are today.
