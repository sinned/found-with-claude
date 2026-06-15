# Customer Interview Transcript — Interview #4

*Interviewee: Solo founder, pre-seed (no investors yet, building toward first raise)*
*Date: 2026-06-12*
*Format: 25-minute call*
*Context: Technical founder, 5 years as an engineer before starting company*

---

**Me:** You don't have investors yet, so you're probably not sending formal updates — is that right?

**Them:** Correct. But I will be in about 4 months if the raise goes well. And I've been doing a lot of prep for that. I have a data dashboard I built myself so I can track things like an investor would see them.

**Me:** Tell me about that dashboard.

**Them:** It's a Python script that runs every morning and pulls from our Stripe account, our database, and Plaid for bank balance. Writes everything to a Google Sheet. So I always have yesterday's numbers when I wake up.

**Me:** How long did that take you to build?

**Them:** Probably 12 hours total? Spread over a couple weekends. It's not complicated — mostly just API calls and some formatting logic.

**Me:** [Technical founder has already solved the gathering problem for himself. This is interesting — is he even in the target market?]

**Me:** Does it work?

**Them:** Mostly. The Stripe integration is rock solid. Plaid is finicky — it goes down, the OAuth tokens expire, and then the whole script breaks silently. Like, I'll come back after a few days thinking I have fresh data and realize the Plaid connection had been broken for three days.

**Me:** What do you do when that happens?

**Them:** Go to Mercury directly and manually update the sheet. Which defeats the purpose.

**Me:** [Silent breakage is a real problem. Not just that it breaks, but that you don't know it broke.]

**Me:** If you raise and suddenly need to send weekly investor updates, would you use your current script for that?

**Them:** I'd want to make it more reliable first. And I'd want to add Linear — we use Linear for engineering and investors always want to see what shipped. I never bothered adding it because the API was annoying to deal with.

**Me:** How do other founders who aren't engineers handle this? Do you know?

**Them:** My co-founder group is all technical, so I don't have great data. But I assume they just... do it manually? Like go to each tool and copy the number?

**Me:** That seems to be the pattern. Would you trust a tool that did this for you over your own script?

**Them:** [pause] If it was more reliable than my Plaid integration, yes. Which is a low bar. But I'd want to understand how it handled edge cases. Like, what if a customer payment fails and then succeeds two days later — does that affect MRR? How does it count?

**Me:** What if every number showed the source and the timestamp?

**Them:** That would help. I could at least verify the inputs without going back to the raw API. The timestamp is actually really important — I want to know if the number is from 10 minutes ago or 10 hours ago.

**Me:** Would you pay for a tool like this?

**Them:** Pre-raise, probably not — I have the script and I can fix it when it breaks. Post-raise, when I'm actually sending weekly updates to real investors? Yeah, probably. The script will feel embarrassing by then anyway.

---

## Notes from this interview

**The DIY segment:** Technical founders build their own solution. This is important — they are not in the core target market unless/until their DIY solution fails them. But it tells us something about what the product needs to do: it has to be better than what a competent engineer builds in a weekend.

**Silent failure is a real UX problem:** The script breaks and doesn't tell you. The tool needs to surface errors loudly, not just produce numbers silently.

**Timestamp is important:** Not just "where did this come from" but "when was this pulled." Investors who care about data freshness need this.

**Linear integration is a gap:** Third mention of wanting to show what shipped to engineering. Stripe + Mercury + Linear may be the minimum viable data package.

**Post-raise trigger:** Technical founders who built their own solution will switch when: (a) they're sending real updates to real investors, (b) the DIY solution feels embarrassing or unreliable. Timing matters.

**Edge case literacy:** Engineers ask very specific edge case questions (failed-then-succeeded payments). The product has to have defensible answers to these, or it won't win technical founders.
