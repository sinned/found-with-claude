# Opportunity Map — Example Output
*Generated from messy-founder-notes.md + customer-transcript-1.md + customer-transcript-2.md*

## Summary

The notes and transcripts cluster around one core pain: founders and finance leaders
at B2B SaaS companies spend 2-4 hours per reporting cycle gathering data from multiple
sources (Stripe, Mixpanel, Mercury, Linear, Salesforce, NetSuite) before they can
produce a recurring report. The top opportunity is in automating this data gathering
— specifically for investor updates at the seed-to-Series B stage.

---

## Opportunity Areas

### 1. Investor Update Data Gathering — Score: 14/15
**Pain: 5/5 | Underservice: 4/5 | Founder fit: 5/5**

**What the problem is:**
Seed-stage founders spend 90-120 minutes every Sunday pulling metrics from 4-6 sources
before they can write their weekly investor update. The writing takes 30 minutes. The
gathering takes 3x as long. The format is always the same. The sources are always
the same. This work is purely mechanical.

**What people do today:**
Manual. Go to Stripe, copy MRR. Go to Mercury, find cash balance. Go to Mixpanel,
screenshot WAU. Go to Linear, skim what shipped. Paste into Google Doc. Calculate
burn rate manually. Double-check every number before sending.

**The founder's edge:**
The founder has done this exact workflow at two companies and has talked to 2 people
who have the same problem. The solution is clear in shape (auto-pull from integrations)
but the trust problem is the hard part — founders are afraid to send AI-gathered
numbers to investors without double-checking.

**Key question to answer:**
What would it take for a founder to trust an automated number enough to send it to
investors without manually verifying? This is the real product challenge.

---

### 2. Board / Leadership Reporting Automation — Score: 11/15
**Pain: 4/5 | Underservice: 3/5 | Founder fit: 3/5**

**What the problem is:**
Finance leaders at Series A-B companies spend 3-4 hours preparing bi-weekly leadership
decks, with most of the time spent reconciling data across Salesforce and NetSuite
(which never match). The reconciliation is not just tedious — it is professional risk.

**What people do today:**
Manual with BI tools that only solve part of the problem. Looker reduces friction for
operational reporting but finance leaders still do leadership reporting manually because
they need auditability at every number.

**The founder's edge:**
Weaker than opportunity #1. The reconciliation problem requires deep accounting domain
knowledge. The distribution is also harder — finance leaders are not usually the buyer.

**Key question to answer:**
Is the reconciliation problem solvable without deep accounting integration? If the
product cannot handle multi-system reconciliation, it only solves the easy part.

---

### 3. Recurring Report Automation (General) — Score: 8/15
**Pain: 3/5 | Underservice: 3/5 | Founder fit: 2/5**

**What the problem is:**
Many knowledge workers produce recurring reports from data spread across systems.
The pain exists beyond founders and finance teams — sales, marketing, and ops managers
all have versions of this workflow.

**What people do today:**
Mix of manual work, BI tools, and custom scripts. This is a crowded space — Zapier,
Supermetrics, Glean, and dozens of others have tried to solve adjacent versions of this.

**The founder's edge:**
Very low. The generic version of this problem is not differentiated. Narrow to a
specific workflow (investor updates) to have founder fit.

**Key question to answer:**
Is there a defensible niche that is genuinely underserved, or is this too crowded?

---

## What to do next

**If you pursue #1:** Talk to 5 more founders specifically about trust. The gathering
problem is clear. The trust problem is the product challenge. Probe: "When do you
stop double-checking a number? What would make you trust an automated number?"

**If you are unsure between #1 and #2:** #1 has better founder fit and a more
obvious distribution path (seed-stage founders are reachable). #2 is technically
harder and has a less clear buyer. Start with #1.

**Before building:** Understand whether the trust problem is solvable without
being explicitly auditable (show the sources inline). The word "auditable" came
up in interview #2 unprompted. Assume it is a requirement.
