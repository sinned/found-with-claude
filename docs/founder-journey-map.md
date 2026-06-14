# Founder Journey Map

The full company-building loop, from raw idea to Demo Day — and the Claude skill
that accelerates each phase.

---

## The loop

```
Problem → Customers → Synthesis → Strategy → Prototype → Users → PMF → Growth → Hire → Raise → Demo Day
   ↑                                                                                               ↓
   └───────────────────────────────── What did we learn? ─────────────────────────────────────────┘
```

Each phase answers one urgent founder question. Each has a skill.

---

## Phase map

| Step | Phase | Core question | Skill |
|------|-------|---------------|-------|
| 1 | Find a problem | Is this pain real and underserved? | `/founder-opportunity-map` |
| 2 | Customer discovery | Who has this problem, exactly? | `/customer-discovery-synthesizer` |
| 3 | Customer simulation | What would real users say about this? | `/synthetic-customer-panel` |
| 4 | Product strategy | What should we build and why? | `/product-strategy-brief` |
| 5 | Prototype | Can we build a working version fast? | `/prototype-scope` → `prototype-with-claude` |
| 5 | Prototype review | Does the prototype prove the thesis? | `/prototype-review` |
| 6 | First users | Who are the first 10 users and how do we reach them? | `/first-users-outreach` |
| 7 | PMF sprint | Are we seeing the signals that matter? | `/pmf-signal-review` |
| 8 | Growth experiments | What lever do we pull next? | `/growth-experiment-backlog` |
| 9 | Hiring | Who is the right first hire? | `/founder-hiring-scorecard` |
| 10 | Fundraising | What is the story investors need to hear? | `/fundraising-narrative` |
| 11 | Demo Day | Can we land this in 2 minutes on stage? | `/demo-day-script` |
| Ongoing | Review | What did we learn? | `/weekly-founder-review` |

---

## The founder learning loop

Every phase feeds back. Prototype review sends you back to customer discovery.
PMF signals reshape product strategy. Growth experiments reveal new customer segments.

The loop is intentional. Founders who compress the loop faster win. Every skill in
this pack is designed to compress one phase of the loop — turning days into hours,
hours into minutes, and minutes into structured decisions.

Claude's role: turn raw founder material into structured insight fast enough that
the bottleneck is learning and judgment, not writing and synthesis.

---

## Key handoffs

### Problem → Strategy

```
/founder-opportunity-map
        ↓
/customer-discovery-synthesizer
        ↓
/synthetic-customer-panel
        ↓
/product-strategy-brief
```

Each skill takes the output of the previous one as input. Run them in sequence.
After `/product-strategy-brief`, you have enough to scope a prototype.

**What you have after these four skills:**
- A ranked map of problem areas (opportunity memo)
- A synthesis of what real customers say (interview synthesis)
- A stress-test of your concept against simulated users (panel output)
- A one-page brief: target customer, core problem, key bets (product brief)

### Strategy → Prototype

```
/prototype-scope
        ↓
Open https://github.com/sinned/prototype-with-claude
Build the skill / validate behavior
        ↓
/prototype-review
```

`/prototype-scope` defines what to build and what success looks like.
The sibling repo `https://github.com/sinned/prototype-with-claude` is where you build it.
`/prototype-review` evaluates the result against the original strategy.

See `docs/prototype-with-claude-integration.md` for the full handoff context.

### Prototype → Users → PMF

```
/first-users-outreach
        ↓
(run for 2-4 weeks, collect signals)
        ↓
/pmf-signal-review
        ↓
/growth-experiment-backlog
```

The prototype gets users. Users generate signals. Signals become experiments.
This loop should run weekly after you have 10+ active users.

**Signs you are ready to move from users → PMF:**
- At least 10 users who have used the product more than once
- At least 3 users who would be "very disappointed" if it went away
- At least 1 user who has told someone else about it unprompted

### PMF → Fundraising → Demo Day

```
/founder-hiring-scorecard    (hire while building PMF evidence)
        ↓
/fundraising-narrative       (build the story from real traction)
        ↓
/demo-day-script             (compress the narrative to 2 minutes)
```

`/fundraising-narrative` and `/demo-day-script` work best when you have real PMF
signals. Investors fund traction, not slides. Run these skills only after you have
data to point to — not after you have a good story.

**The anti-pattern:** running `/fundraising-narrative` before `/pmf-signal-review`.
A narrative built without traction evidence is a hypothesis presentation. Wait for
at least 4-6 weeks of user data before writing the fundraising narrative.

---

## Running the weekly review

`/weekly-founder-review` is the one skill that crosses all phases. Run it every
Friday (or Monday morning). It forces three questions:

1. **What did we learn this week?** (observations, signals, surprises)
2. **What did we ship or do?** (actions taken, decisions made)
3. **What is the single most important thing to do next week?**

The weekly review is also where you decide whether to continue the current phase
or loop back. If the PMF signals are weak after 4 weeks, the right call is often
to return to customer discovery, not to run more growth experiments.

See `journeys/idea-to-demo-day.md` for the full worked example.

---

## The Demo Day moment

Step 11 is Demo Day. If you have followed the journey:

- You know the problem is real (you have synthesis from 10+ interviews)
- You know who has it (you have a clear target customer)
- You have built something that works (validated prototype)
- You have users who use it (first users, PMF signals)
- You have a growth plan (experiment backlog)
- You can tell the story in 2 minutes (Demo Day script)

`/demo-day-script` is the last skill. It takes everything you have built and
compresses it into the 2-minute presentation that determines whether investors
want to meet you.

The script is not a summary of your work. It is an argument that you have found
a real problem, that you are the right team to solve it, and that the traction
you have shows this is working. Every sentence serves that argument.

See `docs/yc-style-demo-day-track.md` for the full YC-style Demo Day framework.
