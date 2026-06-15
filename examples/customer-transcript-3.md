# Customer Interview Transcript — Interview #3

*Interviewee: Co-founder & CEO, seed-stage SaaS company (~12 employees)*
*Date: 2026-06-12*
*Format: 30-minute call*
*Referred by: Interview #1*

---

**Me:** Walk me through how investor updates work at your company. Who sends them, what goes in them, how often?

**Them:** That's me. Every two weeks. I keep saying I'm going to make it weekly but I can never get my act together to do it that often. So biweekly.

**Me:** What does "getting your act together" actually mean there?

**Them:** The data is the problem. I can't sit down and write the update until I have the numbers in front of me, and getting the numbers takes longer than writing the thing. So I keep putting it off.

**Me:** Tell me more about that. What data are you pulling?

**Them:** MRR from Stripe. ARR is just that times 12. Cash from Mercury — I keep a simple spreadsheet where I track runway manually, but the starting point is always the Mercury balance. And then headcount because we've been hiring. And new logos — I count those manually in our CRM.

**Me:** How long does gathering those take you?

**Them:** If I sit down and just do it? Maybe 45 minutes. But I usually don't "just do it." I open Stripe, get distracted by some transaction I need to investigate, go back, forget where I was. It ends up being an hour and a half spread across a Sunday afternoon.

**Me:** What's the investigating-a-transaction thing?

**Them:** Like, I'll pull the MRR number and it'll be lower than last week, and I have to figure out why. Did someone churn? Was it a payment failure? That's not really the update's problem but once I see it I can't not look.

**Me:** [Interesting — data gathering triggers other work. Not just time cost, but attention cost.]

**Me:** Have you tried to automate any of the gathering?

**Them:** We use Baremetrics, which automatically pulls from Stripe. So the MRR number is always there without me having to go to Stripe directly. But I still end up going to Stripe because I don't fully trust Baremetrics on edge cases.

**Me:** What edge cases?

**Them:** Like when we have a customer on a custom contract, or when there's a refund, or when we upgraded someone mid-month. Baremetrics gets confused and I've caught it being wrong a few times. So now I check.

**Me:** [Pattern from Interview #2 — the tools exist but founders don't trust them, especially on edge cases.]

**Me:** If you had something that gathered all of this for you and you trusted it completely, what would change?

**Them:** The updates would go out on time. Which sounds small but it actually matters — investors notice when updates are late. I've had investors email me to ask if everything is okay when I missed one. That's not a conversation I want to have.

**Me:** What would it take to trust AI-gathered numbers?

**Them:** The Baremetrics problem makes me nervous about this. I think I'd need to see the logic — like, here's how we calculated MRR and here are the inputs. Not just the number but how we got there.

**Me:** Would source links be enough? Like, "this MRR came from Stripe, as of Tuesday at 9pm, and here are the subscription IDs that make it up"?

**Them:** That would be way better than what I have now. If I could see the components, I could spot if something was wrong without re-pulling from Stripe. Yeah, that would help.

**Me:** What would you pay for that?

**Them:** [pause] We're pretty scrappy on tools right now. Probably $50/month? Maybe $75 if it was really solid. We're not a big team.

---

## Notes from this interview

**Key pattern confirmed:** The "biweekly instead of weekly" dynamic is a consequence of the data gathering problem. The update cadence is being driven by the friction of gathering, not by what investors want.

**New insight — attention cost:** Data gathering doesn't just cost time, it triggers unrelated work (investigating transactions). The context-switching cost is real and hard to quantify.

**Baremetrics comparison:** Third interviewee in a row who uses some form of automation but still double-checks manually. The tools exist; the trust doesn't. This pattern is very consistent.

**Edge cases are the real problem:** Custom contracts, refunds, mid-month upgrades. These are exactly the cases where automated tools break. A good solution has to handle or at least flag these.

**Price sensitivity:** Lower than Interviews #1 and #2. Seed stage, scrappy. $50-75/month vs. the "I'd pay $200/month" signal from Interview #1. Pricing will depend heavily on stage.

**The lateness problem:** Investors notice and worry when updates are late. This is a reputational/relationship cost the founder didn't want to name explicitly but it's clearly there.
