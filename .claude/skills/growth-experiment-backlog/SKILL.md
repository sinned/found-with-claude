---
name: growth-experiment-backlog
description: Generate a prioritized backlog of growth experiments based on PMF signals and the current growth bottleneck. Produces experiment cards with hypothesis, metric, and effort estimate. Use when you have early PMF signals and want to grow. Trigger phrases: "growth experiments", "how do we grow", "what lever should we pull", "build a growth backlog", "next growth steps".
---

# Growth Experiment Backlog

Takes PMF signals and the current growth bottleneck and produces a prioritized
backlog of growth experiments — each with a clear hypothesis, the metric to move,
and an effort estimate.

## Input

Look for:
- `work/pmf-signal-review/pmf-signal-review-output.md` — what is working and what is not
- The founder's description of the current bottleneck:
  - "We have users but they're not activating"
  - "Users activate but don't retain"
  - "Users retain but don't refer"
  - "We can't get enough users to try it in the first place"
- Any current growth metrics the founder shares

If the PMF signals are weak: say so before generating experiments. Growth
experiments on weak PMF waste time. Recommend returning to `/pmf-signal-review`
or `/customer-discovery-synthesizer` first.

## Steps

1. **Identify the bottleneck** — From the PMF memo and founder context, where is
   growth breaking down? The bottleneck determines which experiments to prioritize.
   Common bottlenecks:
   - **Acquisition:** Not enough people are hearing about this
   - **Activation:** People hear about it but do not try it
   - **Retention:** People try it but do not come back
   - **Referral:** People use it but do not tell others

2. **Generate experiments for the bottleneck** — Generate 8-12 experiments
   targeted at the primary bottleneck. For each, define:
   - The hypothesis (If we do X, we expect Y because Z)
   - The metric to move
   - The effort (Low / Medium / High)
   - The time to signal (how quickly will we know if it worked?)

3. **Generate a few experiments for the secondary bottleneck** — Do not ignore
   the second bottleneck entirely. 2-3 experiments here.

4. **Prioritize** — Score each experiment on:
   - Expected impact (High / Medium / Low)
   - Effort (Low = 1-2 days, Medium = 1 week, High = 2+ weeks)
   - Time to signal (Fast = <2 weeks, Slow = 4+ weeks)

   Prioritize: high impact, low effort, fast signal first.

5. **Select the top 3** — The experiments to run this week. Never run more than
   3 experiments at once — you cannot learn from 10 simultaneous variables.

6. **Write the experiment cards** for the top 3 in detail.

7. **Write the backlog** — Follow the output format below.

8. **Save output** — Write to `work/growth-experiment-backlog/growth-experiment-backlog-output.md`.

## Output format

```markdown
# Growth Experiment Backlog
*Generated: [date] | Primary bottleneck: [Acquisition / Activation / Retention / Referral]*

## Current situation
[2-3 sentences: what is working, what is the bottleneck, what we are trying to do]

---

## This week: run these 3 experiments

### Experiment 1: [Name]
**Hypothesis:** If we [action], then [metric] will [direction] because [reason].
**Primary metric:** [Specific, measurable metric]
**Time to signal:** [X days / weeks]
**Effort:** [Low / Medium / High] — [Estimated hours]
**How to run it:**
1. [Step 1]
2. [Step 2]
3. [Step 3]
**What we will learn:** [What a positive result means / what a negative result means]

---

### Experiment 2: [Name]
[Same structure]

---

### Experiment 3: [Name]
[Same structure]

---

## Full backlog

### Acquisition experiments
| Experiment | Impact | Effort | Time to signal | Priority |
|-----------|--------|--------|----------------|----------|
| [Experiment A] | High | Low | 1 week | Run now |
| [Experiment B] | High | Medium | 2 weeks | Next |
| [Experiment C] | Medium | Low | 1 week | Next |

### Activation experiments
[Same structure]

### Retention experiments
[Same structure]

### Referral experiments
[Same structure]

---

## What not to run right now
| Experiment | Why not yet |
|-----------|------------|
| [Experiment] | [Reason: too early, wrong bottleneck, waiting on data] |

---

## Success criteria for this week's experiments

At the end of [X] weeks, we will review results and decide:
- **If Experiment 1 works:** [What we do next]
- **If Experiment 1 fails:** [What we conclude and what we try instead]
- **If all three fail:** [What this tells us about the bottleneck or the product]
```

## Growth experiment principles for early startups

**Do not run paid ads until you have manual traction.** If you cannot get users
one by one, money will not change that. Paid acquisition reveals channel efficiency,
not product-market fit.

**The fastest growth loop at this stage is personal.** Send 5 personal messages.
Get 3 users. Watch them. Learn more in 1 week than in 1 month of funnel analysis.

**One metric per experiment.** If you change the onboarding email AND the welcome
screen at the same time, you will not know which one moved the metric.

**Define "works" before you run it.** An experiment without a clear success
threshold is just activity. Write: "This works if [metric] moves by at least [X%]
within [Y days]."

**Stack rank by bottleneck.** If your retention is 10%, fixing acquisition will
just fill a leaky bucket. Fix retention first.
