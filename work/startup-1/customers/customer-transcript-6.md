# Customer Interview Transcript — Interview #6

*Interviewee: Founder & CEO, seed-stage company (~8 employees)*
*Date: 2026-06-13*
*Format: 40-minute call*
*Background: 4 years as a financial analyst before founding. High skepticism of automation.*

---

**Me:** I'm researching investor update workflows — specifically the data gathering part. Walk me through yours.

**Them:** Sure. Weekly updates, every Sunday. I have a spreadsheet I've maintained for two years. Every Sunday I go to each source and fill it in. Stripe MRR, Mercury cash, product metrics from our analytics tool, deals from our CRM.

**Me:** Two years — that's a long time to maintain a manual spreadsheet. Why not automate it?

**Them:** I've thought about it. I've tried a couple of things. But here's the thing — I was a financial analyst for four years before this. I've seen what happens when people trust automated reports they don't understand. They put the wrong numbers in a presentation and it's embarrassing at best, catastrophic at worst. I'd rather spend 90 minutes being sure than 10 minutes being surprised.

**Me:** [This is the skeptic. Finance background. Automation aversion is principled, not just habitual.]

**Me:** Tell me about the things you tried.

**Them:** I connected Stripe to a Notion database once. It was pulling the right number for about three months and then it started pulling gross revenue instead of MRR and I didn't notice for a few weeks. Once I caught that I shut it off.

**Me:** How did you catch it?

**Them:** My MRR number was growing faster than I expected. It felt wrong. So I went to Stripe directly and compared. The numbers didn't match.

**Me:** [Interesting — he caught the error because he had a mental model of what the number should be. That's a form of internal audit.]

**Me:** What would have happened if you hadn't noticed?

**Them:** I would have sent inflated MRR numbers to my investors. For three weeks before I caught it. That's not okay. Investors make decisions based on these numbers. If I'm wrong by 15% and they find out later, I've lost their trust.

**Me:** What would it take for you to trust an automated system enough to use it for investor updates?

**Them:** [long pause] I want to say "nothing" but that's probably not fair. Let me think. I think I'd need to understand exactly how it calculated the number. Not just "Stripe MRR" — I'd want to know: what subscriptions does it include? How does it handle annuals? What does it do with failed payments?

**Me:** What if every number came with a breakdown — the list of subscriptions that were included, clearly stamped with the timestamp?

**Them:** That would help. I could spot-check it. But I'd spot-check it every week for at least the first few months.

**Me:** Would you eventually stop spot-checking?

**Them:** If it was right 20 times in a row? Maybe. I'm not going to pretend I'd check forever. But the bar is higher than it is for most people.

**Me:** That's actually helpful to hear. If it's right 20 times in a row with a clear breakdown, you'd trust it?

**Them:** For the standard metrics, yes. For anything involving custom contracts or unusual billing arrangements, I'd always want to verify. Those are where tools get it wrong.

**Me:** What would you pay for this?

**Them:** Honestly I'm not sure I'd pay for it. I don't love the time it takes, but I also don't think the 90 minutes is the real cost. The real cost is the risk of sending wrong data. If a tool genuinely eliminates that risk, maybe. But I'm skeptical it can.

---

## Notes from this interview

**The principled skeptic:** Finance background creates a specific kind of wariness — not tech-averse, but trained to distrust numbers you didn't compute yourself. This is a real and legitimate objection.

**Error detection through intuition:** He caught the Notion error because "the number felt wrong." This is a key insight: experienced founders have a mental model that acts as a sanity check. Newer founders might not have this, which makes the trust problem worse for them.

**The bar for trust:** 20 consecutive correct results. This is much higher than earlier interviewees. The trust threshold scales with risk aversion and financial sophistication.

**Custom contracts as the exception:** Every interviewee has mentioned custom contracts or unusual billing as the place automation breaks. This is likely true. The product needs to either (a) handle these correctly, (b) flag them as exceptions, or (c) be honest that they're out of scope.

**Low/zero WTP:** This interviewee might not be a buyer at any price. The time savings don't motivate him because time isn't his core concern — accuracy is. If the product can't credibly address accuracy, this segment won't convert.

**Important for the product:** The tool needs to be transparent enough that even this type of customer can audit it. The breakdown view (which subscriptions are included, how annuals are handled) is table stakes for this segment.
