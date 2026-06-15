# Customer Interview Transcript — Interview #2

*Interviewee: Head of Finance, Series B SaaS company (~120 employees)*
*Date: 2026-06-11*
*Format: 40-minute call*
*This interview explores whether the pain exists for finance leaders, not just founders*

---

**Me:** Thanks for talking with me. I'm researching how finance teams at Series B 
companies handle regular reporting — specifically the data gathering part, not the 
analysis part. What does your weekly reporting cycle look like?

**Them:** It's actually every two weeks for us. We have a leadership sync every other 
Tuesday where I present the business metrics — revenue, pipeline, headcount, cash. 
I prepare a slide deck the day before.

**Me:** Walk me through how you prepare that deck.

**Them:** I have a template that I update. So I go to Salesforce first and pull the 
current quarter's bookings and pipeline. Then I go to NetSuite for the financials — 
revenue, expenses, cash. Then I have a separate spreadsheet where we track headcount 
manually because our HRIS doesn't have good reporting. And then I check in with the 
data team for any product metrics they want to include.

**Me:** How long does that take?

**Them:** If everything goes smoothly? Three, four hours. But it often doesn't. 
Salesforce data is almost always stale or wrong in some way. Someone didn't close 
a deal they closed last week, or there's a duplicate. I spend a lot of time 
reconciling.

**Me:** What do you mean, reconciling?

**Them:** Like the revenue in Salesforce won't match the revenue in NetSuite. And 
I have to figure out why, and sometimes it's a legitimate accounting difference and 
sometimes it's a data entry error. I can't put a number in a leadership deck that's 
wrong. So I have to check it.

**Me:** [Different problem than the founder — not just gathering, but data 
quality and reconciliation]

**Me:** Have you tried to automate any of this?

**Them:** We use a BI tool — Looker — for some of it. But I still end up doing a 
lot manually because I don't trust the numbers until I've traced them back to source. 
The Looker dashboard is mostly for the sales team. For leadership reporting, I need 
to know every number is right.

**Me:** Why is that — why do you need to be so sure?

**Them:** [slight pause] Because if I put a wrong number in front of our CEO or our 
board, that's a really bad day. The whole point of the CFO role is to be the person 
who knows the numbers. If I'm presenting wrong numbers, what's my job?

**Me:** [Key insight: the trust issue is professional identity, not just accuracy]

**Me:** If you had something that could reliably gather and reconcile these numbers 
for you — and you trusted the output — what would you do with the time?

**Them:** I'd spend it on actual analysis. Right now I'm spending 80% of my time 
on data plumbing and 20% on "what does this mean." I would love to flip that.

**Me:** What would it take for you to trust an automated number enough to put it in 
a leadership deck?

**Them:** [long pause] That's a really good question. I think I'd need to see it 
match what I compute manually at least 10 times in a row before I stopped 
double-checking. Maybe more. It would have to be auditable — I need to see where 
every number came from, not just the number.

**Me:** Auditable — meaning what exactly?

**Them:** Like, I should be able to click on the MRR number and see: "This came 
from Stripe, as of 11pm last night, and here are the 5 deals that make it up." 
If it's a black box, I will never trust it.

---

## Notes from this interview

**Key difference from Interview #1:** Finance leader's problem is data quality and 
reconciliation, not just gathering speed. The core fear is professional — presenting 
wrong numbers is a career risk. The product needs to be auditable, not just fast.

**The quote that matters:** "I should be able to click on the MRR number and see 
where it came from." Auditability is non-negotiable for this customer type.

**Potential customer segment split:**
- Founders want speed (get the gathering done so they can write)
- Finance leaders want auditability (make it trustworthy, speed is secondary)
These might be different products, or at minimum, different feature priorities.

**Surprising thing:** Finance leader uses Looker but still does the leadership 
reporting manually. The BI tool reduced friction for some reports but not the 
ones that matter most. This is a pattern worth exploring.

**Next question:** Is the finance leader the buyer, or does IT/RevOps need to 
approve? This affects distribution strategy significantly.
