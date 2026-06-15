# Customer Interview Transcript — Interview #9

*Interviewee: YC W25 founder, post-batch (~10 employees)*
*Date: 2026-06-14*
*Format: 30-minute call*
*Context: Graduated YC 6 months ago, sends weekly updates to YC partners + angels*

---

**Me:** You came out of YC recently. How did YC's update expectations shape how you send updates now?

**Them:** YC trains you to do weekly updates. Weekly. They check — they have a system where you log your metrics and write a short update, and partners read them. So you don't miss one.

**Me:** And now that you're post-batch?

**Them:** I still do it weekly. My angels expect it now. The habit is in place. But the tooling that YC provided was specific to YC's system — now I'm just sending an email.

**Me:** What's in the email?

**Them:** MRR, WAUs, cash runway, top win, top challenge, biggest question I'm wrestling with. Usually about 300 words.

**Me:** How long does it take?

**Them:** The writing is fast — 20 minutes. The data is slower. Stripe I go to directly. We use Amplitude for product analytics. Mercury for cash. And we use Notion for project tracking, which I don't bother pulling because it's too unstructured.

**Me:** Total time?

**Them:** Probably 50-60 minutes per week. So maybe 4 hours a month.

**Me:** How do you feel about that?

**Them:** I know it's valuable. The investors who read the updates are more helpful to me than the ones who don't. But 4 hours a month is real. We're 10 people. That's time I could spend on product or sales.

**Me:** If you could reduce the data gathering part to 5 minutes, would you?

**Them:** Obviously yes.

**Me:** What would you need to trust the numbers enough to just use them without checking?

**Them:** I'm pretty trusting on this stuff as long as I can see the source. I've built enough API integrations that I know how they work. If I can see it's pulling from Stripe's API and not some cached version, I'm fine.

**Me:** [Developer-adjacent founder — lower trust bar, but specific requirements about data freshness.]

**Me:** What's the "cached version" concern?

**Them:** Some reporting tools pull from Stripe webhooks, not the API directly. Which means if a webhook failed, you might have stale data and not know it. I want the data pulled at the time of the update, not stored somewhere.

**Me:** That's a specific technical requirement. Do you know if that's a common concern?

**Them:** Among technical founders, yeah. Non-technical founders probably don't think about this.

**Me:** What would you pay for a tool that pulled fresh data and pre-filled your weekly update template?

**Them:** $100/month, easy. YC batch gave us a bunch of SaaS credits so I'm a little used to things being free, but for something I use weekly that saves me an hour? Yes.

**Me:** Any features that would make you not use it?

**Them:** If it put YC-style formatting on the update. My angels have different preferences than YC partners do. I need to write my own update, not use a template someone else designed.

---

## Notes from this interview

**YC-trained founders send every week:** This creates a strong habit and a specific expectation from investors. The product should target post-YC founders as a distribution channel — they have the habit, they just need better tooling.

**The webhooks vs. API distinction:** A real technical concern that non-technical founders won't raise. Pull fresh from the API, not from cached webhook data. This needs to be in the product spec.

**WTP $100/month:** Slightly lower than other similar-stage founders. Post-YC SaaS credits may be suppressing perceived price. But still clear willingness.

**Anti-feature: imposing format.** Multiple founders now have said they don't want the tool to define their update format. The tool should pre-populate data into the founder's format, not force a template.

**Data freshness timestamp matters:** Confirming Interview #4's insight. "Pulled at the time of the update" is a specific requirement. The timestamp in the source tag isn't just nice-to-have — it's the evidence of freshness.

**Distribution insight:** YC alumni Slack groups are a logical GTM channel. Founders trained to send weekly updates are already the converted customer — they just need better tooling.
