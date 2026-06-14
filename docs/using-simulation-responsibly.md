# Using Simulation Responsibly

The `/synthetic-customer-panel` skill simulates customer reactions. This document
explains what simulation can and cannot do, and how to use it without fooling yourself.

---

## What synthetic panels are good for

**Generating hypotheses.** A synthetic panel will not tell you what customers
actually think. It will surface objections, edge cases, and questions that you
might not have thought to test in real interviews. These become hypotheses — things
to probe in the next real conversation.

**Pressure-testing a concept before you build it.** If 4 of 5 synthetic archetypes
say "I would never share this data with an external tool," that is a signal to
investigate, not to dismiss. It does not mean the concern is real — it means you
should find out.

**Preparing for customer conversations.** The objections raised by a synthetic
panel are often the same objections real customers will raise. Running the panel
before a founder call gives you language to use and answers to prepare.

**Moving faster when real interviews are not possible.** Between interview rounds,
the synthetic panel lets you keep iterating on the concept without waiting for
scheduled calls.

---

## What synthetic panels cannot do

**Replace real customer discovery.** Synthetic panels are trained on patterns
from public data. They reflect generic startup knowledge about how personas
"typically" behave. They do not know the specific context of your specific
customers in your specific market.

**Validate demand.** A synthetic customer saying "yes, I would pay for this"
is not evidence of demand. It is a simulation of a reasonable response. Real
demand comes from real people opening their wallets or changing their behavior.

**Catch unknown unknowns.** The panel can only surface objections that the model
has seen before. The most dangerous objections — the ones that kill startups —
are often specific, contextual, and invisible to simulation.

**Replace talking to 5 real customers.** If you are deciding between running a
synthetic panel and doing 5 more customer interviews, do the interviews.

---

## The responsible use pattern

**Before building:**
1. Run `/customer-discovery-synthesizer` on real interviews first
2. Use the synthesis to define your concept clearly
3. Run `/synthetic-customer-panel` to generate objection hypotheses
4. Return to real customers to test those hypotheses

**When you get a concerning panel result:**
- Do not dismiss it ("the simulation doesn't understand our market")
- Do not treat it as confirmed ("users will definitely hate this")
- Treat it as a hypothesis: "We should probe this objection in the next call"

**When you get an encouraging panel result:**
- Do not use it as validation ("even the simulation thinks this will work")
- Treat it as a signal: "Our concept passes the basic sanity check. Now let's
  talk to real people."

---

## How to frame panel output when sharing

If you share synthetic panel output with a co-founder, investor, or advisor,
be explicit about what it is:

> "These are simulated reactions — not real customer feedback. I ran this to
> identify which objections to probe in our next interviews."

The most common misuse: presenting synthetic panel output as if it were real
customer research, because it looks similar on the page. Do not do this.
Investors and advisors who discover this lose trust quickly.

---

## A note on the model's limitations

The synthetic panel creates archetypes based on patterns in the model's training data.
It will perform better on well-understood customer segments (enterprise SaaS buyers,
early adopters in tech) than on niche or novel segments (buyers in regulated industries,
specific professional roles in specific geographies).

For niche segments: use the panel to generate questions, not conclusions. Then go
find 3 real people in that segment and ask them directly.

---

## The honest version of the skill

`/synthetic-customer-panel` is useful. It is also a shortcut. The best founders
use it as a forcing function to sharpen their concept and prepare for the next
real interview — not as a substitute for doing the interviews.

The real panel is in your customer's office. Go there.
