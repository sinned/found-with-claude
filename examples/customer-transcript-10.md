# Customer Interview Transcript — Interview #10

*Interviewee: Founder & CEO, seed-stage marketplace (~20 employees)*
*Date: 2026-06-14*
*Format: 35-minute call*
*Context: Non-SaaS business — marketplace model. Different metrics than recurring revenue.*

---

**Me:** Walk me through your investor update process.

**Them:** Monthly. It goes out the first Monday of the month, without fail — my investors are really engaged and they'd notice if I was late. I have an ops person who helps me draft it.

**Me:** What data goes in it?

**Them:** GMV — gross merchandise value — is the headline metric. Then take rate, which gives you the implied revenue. Supply count and demand count — how many sellers, how many buyers. And cash runway.

**Me:** Where does that data live?

**Them:** GMV and take rate come from our internal database — we have a custom analytics query that our engineer runs. Supply and demand come from our CRM. Cash from Mercury.

**Me:** You have an engineer run a custom query every month?

**Them:** Yeah. It takes them about 20 minutes. But it means I have to schedule it — ping the engineer, wait for them to run it, get back the number. It adds a whole coordination step.

**Me:** [Different problem than SaaS founders — bespoke database queries, not off-the-shelf APIs. The data sources are more custom.]

**Me:** Have you tried to automate the query?

**Them:** We built a simple internal dashboard. But the dashboard shows the current number — I need the number as of the last day of the month, not today. So I still have to ask the engineer to run the query for that specific date range.

**Me:** What about Mercury and the CRM data?

**Them:** Mercury I do myself — 5 minutes. CRM is messier — the supply and demand counts include some test accounts and internal accounts and I have to filter those manually. Or I ask my ops person to, which adds another coordination step.

**Me:** It sounds like the coordination is the main pain, not just the time.

**Them:** That's exactly right. I need 4 different people or systems to give me something before I can write. And I need them to give it to me at the same time, which never happens.

**Me:** [Important framing for this customer: the problem isn't just data gathering, it's orchestration across people and systems.]

**Me:** If you had a tool that gathered the data automatically — assuming your data lives in standard APIs — would it solve the problem?

**Them:** For some of it. Mercury, yes. The GMV stuff, no — that's in our own database. Unless you connect to our database directly, which... I don't know how I feel about that.

**Me:** What would make you comfortable connecting your database?

**Them:** Read-only access, obviously. A clear privacy policy. And I'd want to know exactly what queries you're running, not a black box.

**Me:** The transparency requirement again. What would you pay for a solution that handled what it could?

**Them:** If it handled Mercury and the CRM parts reliably, I'd pay maybe $100-150/month. The database stuff would be a bonus, not the core value. Honestly, just getting me the cash runway and supply/demand without coordination overhead would be useful.

**Me:** Last question — do other marketplace founders have this problem?

**Them:** Every marketplace founder I know has bespoke analytics. None of us use Stripe in the same way SaaS companies do. This might be a different product entirely for us.

---

## Notes from this interview

**The marketplace segment:** Non-SaaS businesses have fundamentally different data sources. GMV, take rate, supply count, demand count — these don't live in Stripe. A SaaS-focused product may not solve their problem.

**Orchestration as the core pain:** Not just gathering data, but coordinating across people, systems, and timing. This is a different problem from the solo-gathering problem of SaaS founders.

**Custom database queries:** A category of data that off-the-shelf API integration can't handle. The product would need a "bring your own query" feature or just have to exclude this segment.

**Transparency for database access:** Read-only + visible queries is the trust bar for connecting production databases. This is actually achievable.

**Potential segment split:** The SaaS founder segment (Stripe + Mercury + analytics tool) is much more addressable with a v0 than the marketplace segment. Start SaaS, expand later.

**WTP lower for partial solution:** $100-150/month when the tool only solves part of the problem. This confirms that the more complete the data package, the higher the WTP.
