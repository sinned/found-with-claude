# Idea to Demo Day: The 12-Week Journey

A worked example of the full founder journey using the skills in this pack.
Based on a fictional founder building an investor update automation tool.

---

## The premise

**Founder:** Sofia, ex-Head of Revenue Operations at two Series B SaaS companies
**Problem:** Founders spend hours gathering data before writing investor updates
**Starting point:** A hunch + 2 customer interviews + a strong stomach for feedback

---

## Week 1 — Find a problem

**Skill used:** `/founder-opportunity-map`
**Input:** Sofia's RevOps background, a few conversations with founder friends, messy notes

**What happened:**
Sofia ran the opportunity map with her notes. The output ranked investor update
data gathering as the #1 opportunity. The key insight: the format never changes,
the sources are always the same, and the automation problem is actually about trust,
not technology.

**Output:** Opportunity memo with 3 ranked areas and a clear "key question to answer"
for each.

**Week 1 decision:** Pursue opportunity #1. Talk to 5 more founders specifically
about trust.

See `journeys/week-01-find-a-problem.md` for the detailed account.

---

## Week 2 — Customer discovery

**Skill used:** `/customer-discovery-synthesizer`
**Input:** 7 customer interviews (5 seed-stage founders, 2 Series A)

**What happened:**
Sofia ran 7 interviews in 5 days. She dropped all transcripts in `examples/`.
The synthesis revealed three consistent patterns:
1. Data gathering > writing time (7/7 interviews)
2. Format never changes (6/7)
3. Trust is the core barrier to automation (5/7)

Most surprising: 3 of 7 founders mentioned using a shared Slack group where they
complained about investor updates together. Distribution insight.

**Output:** Customer synthesis with patterns, quotes, and open questions.

**Week 2 decision:** The problem is real. The hard part is trust. Proceed to simulation
to stress-test the concept before writing the product brief.

---

## Week 3 — Customer simulation

**Skill used:** `/synthetic-customer-panel`
**Input:** Customer synthesis + concept: "auto-pull Stripe + Mercury + Linear data into a weekly update draft"

**What happened:**
The panel surfaced 3 archetypes who were excited and 2 who had blockers:
- Archetype 4 (finance-minded founders): "I would not send numbers I haven't checked.
  Full stop." — trust objection confirmed
- Archetype 5 (early-stage, pre-traction): "I don't have Stripe yet" — scope question

Most important output: "The strongest objection is auditability. If the numbers
are presented without source links, the finance-minded founder will not adopt."

**Output:** Synthetic panel with 5 archetypes, cross-panel analysis, and 3 hypotheses
to test with real customers.

**Week 3 decision:** Add auditability to the core product concept before writing
the brief. Every number must show its source.

---

## Week 4 — Product strategy

**Skill used:** `/product-strategy-brief`
**Input:** Opportunity memo + synthesis + panel output

**What happened:**
Sofia wrote the product brief. Key decisions made in this session:
- Target customer: seed-stage founders (not Series A with dedicated finance)
- Core job: auto-gather data from Stripe + Mercury + Linear, formatted for update template
- Out of scope: writing the narrative (founders want to write it themselves)
- Riskiest assumption: founders will trust AI-gathered numbers with source attribution

**Output:** One-page product brief with target customer, solution hypothesis, key bets,
and success criteria for the prototype.

**Week 4 decision:** Ready to scope the prototype. The brief is clear enough.

---

## Week 5 — Prototype

**Skills used:** `/prototype-scope` → prototype-with-claude → `/prototype-review`
**Input:** Product brief

**What happened:**
Sofia ran `/prototype-scope`. The scope came out to one job: "take a seed-stage
founder's Stripe, Mercury, and Linear credentials, pull the current week's data,
and produce a pre-filled investor update template with source links for every number."

Sofia opened `https://github.com/sinned/prototype-with-claude` and used `/new-skill` to create a skill
called `generate-investor-update`. She wrote the SKILL.md in 20 minutes based on
the scope document.

First run: worked for Stripe and Mercury, failed on Linear (API complexity). Scope
was immediately narrowed: drop Linear for v0, add it later.

After two `/improve-skill` cycles, the skill hit 85% on eval criteria.

Sofia ran `/prototype-review`. Verdict: INCONCLUSIVE. The prototype demonstrated
data gathering, but the "trust" test required showing source links inline in the
output — which the first version did not do. The riskiest assumption was not yet tested.

**Week 5 decision:** Rebuild the output format to include source attribution for
every number. Then find 3 founders to try it with real data.

---

## Week 6 — First users

**Skill used:** `/first-users-outreach`
**Input:** Product brief + revised prototype description

**What happened:**
Sofia ran the outreach skill. Output: a warm network message, a referral template,
and a feedback capture guide. The skill identified the Slack group as the best
first channel (multiple interviewees had mentioned it).

Sofia sent 10 personal messages. 6 responded. 4 agreed to try it live.

In 4 live sessions:
- 3 of 4 said the source attribution made them comfortable
- 2 of 4 sent the auto-generated numbers to their investors without manually checking
- 1 asked for Google Sheets instead of a Google Doc (noted as roadmap item)

**Week 6 signal:** 2 of 4 sent without checking. This is the first evidence the
trust problem is solvable.

---

## Week 7 — PMF sprint

**Skill used:** `/pmf-signal-review`
**Input:** Week 6-7 user data: 4 initial users + 3 referrals from those 4 users

**What happened:**
Seven users in 2 weeks. Sofia ran the PMF signal review. Key signals:
- 5/7 used it a second time (71% second-use retention)
- 3/7 referred it to someone without being asked
- The "very disappointed" cluster: founders with 10-20 investors who send weekly

**Verdict:** MIXED SIGNALS. Retention is promising. Sample is too small. Need 20+
users before drawing strong conclusions.

**Week 7 decision:** Expand to 20+ users before writing the fundraising narrative.
Run the growth experiment backlog to decide how to get there.

---

## Week 8 — Growth experiments

**Skill used:** `/growth-experiment-backlog`
**Input:** PMF signal review + current bottleneck (acquisition — 7 users, need 20+)

**What happened:**
Three experiments selected:
1. Post in 3 founder Slack groups (low effort, fast signal)
2. Ask each current user for 2 referrals directly (personal, specific ask)
3. Write a short post about the Sunday evening problem (content as distribution)

Results after 2 weeks: Experiments 1 and 2 worked. 18 new users in 2 weeks. 25 total.

---

## Week 9 — Hiring

**Skill used:** `/founder-hiring-scorecard`
**Input:** Role: first engineer (full-stack, integration-focused)

**What happened:**
Sofia used the skill to define the scorecard before starting interviews. The skill
forced clarity on the actual job: "Build the integrations that are currently breaking
most often (Linear) and create the auth flow so users can connect their own accounts."

Scorecard revealed the must-have: "Has shipped a production API integration before —
not a tutorial, but something real users are using."

Sofia interviewed 5 candidates. The scorecard made the decision clear.

---

## Week 10 — Fundraising

**Skill used:** `/fundraising-narrative`
**Input:** Product brief + PMF signals (25 users, 70% retention, 3 unprompted referrals)

**What happened:**
Sofia wrote the investor memo. The narrative spine:
- Insight: "Founders don't want AI to write their investor updates — they want
  to write it themselves. The problem is the data gathering."
- Traction: "25 users, 70% second-week retention, 3 referred without being asked"
- Ask: "$1.2M seed to hit 200 active users and launch API integrations for the
  top 10 tools founders use"

The objection map revealed the hardest question: "Why won't Stripe / Mercury just
build this?" — Sofia's honest answer: "They might, eventually. We are building for
founders, not for Stripe. By the time Stripe considers this, we will have 2,000 users."

---

## Week 11 — Demo Day

**Skill used:** `/demo-day-script`
**Input:** Fundraising narrative + live demo flow

**What happened:**
The script went through 5 drafts. The hook that worked:

> "Every founder I know dreads Sunday evenings. Not because writing to investors
> is hard — but because finding the data takes 3 hours and the writing takes 30
> minutes. UpdateDraft solves the 3-hour problem. 25 founders are using it.
> 70% came back the second week."

Two-minute Demo Day script. 3 meetings booked in the week after Demo Day.

---

## Week 12 — Post-Demo Day

**Skill used:** `/weekly-founder-review`
**Input:** Everything from the past 12 weeks

**Week 12 reflection:**

What worked: the weekly review kept decisions grounded in evidence. Every major
pivot (dropping Linear from v0, adding source attribution, focusing on seed-stage)
came from a weekly review that surfaced new evidence.

What was hardest: getting to 25 users. The product had to be good enough that
people would recommend it without being asked. That took longer than expected.

What is next: build the integrations pipeline, onboard 200 users, prepare the
seed round close.

---

The journey from idea to Demo Day took 11 weeks. The skills did not make decisions
— Sofia made the decisions. The skills compressed the time between input and insight
at every phase: turning notes into memos, interviews into synthesis, hunches into
structured bets, and numbers into a 2-minute argument that investors wanted to hear.
