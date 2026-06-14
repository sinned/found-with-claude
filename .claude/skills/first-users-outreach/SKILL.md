---
name: first-users-outreach
description: Plan and write outreach to get the first 10 users for a new product. Produces an outreach sequence and a feedback capture template. Use after building a working prototype. Trigger phrases: "get first users", "write outreach", "find beta users", "who should we reach out to".
---

# First Users Outreach

Takes a product brief and prototype description and produces a targeted outreach
plan: who to reach, what to say, and how to capture feedback from early users.

## Input

Look for:
- `examples/product-brief-output.md` — who the target customer is
- `examples/prototype-scope-output.md` — what the prototype does
- `examples/customer-synthesis-output.md` — specific people or companies mentioned in discovery
- Any existing network context the founder mentions ("I know 50 founders in this space")

The goal is the first 10 users, not the first 10,000. This is a manual, personal
outreach plan — not a marketing funnel.

## Steps

1. **Define the ideal first user** — Not the ideal eventual customer. The ideal
   first user is someone who:
   - Has the problem acutely right now
   - Will give you honest feedback (not just be polite)
   - Is reachable by the founder directly
   - Is not so important that a bad experience would be costly

2. **Identify the target list** — From the founder's network and the customer
   discovery context, identify the specific types of people to reach out to.
   Provide 3-5 user types ordered by priority.

3. **Write the outreach messages** — Three versions:
   - **Warm network:** Someone the founder knows directly
   - **Warm intro:** Someone 1-2 hops away (referral request)
   - **Cold (if necessary):** Someone the founder does not know

4. **Define the onboarding ask** — What exactly are you asking first users to do?
   Be specific: "Try this tool on [specific task] and tell me if [specific thing]
   worked." Not: "Check it out and give feedback."

5. **Design the feedback capture** — How will you learn from the first users?
   Specify: session format (live call? async?), what to observe, what questions to ask.

6. **Write the outreach plan** — Follow the output format below.

7. **Save output** — Write to `examples/first-users-outreach-output.md`.

## Output format

```markdown
# First Users Outreach Plan
*Generated: [date] | Target: first [N] users*

## The ideal first user

**Who they are:** [Specific role + context]
**Why them first:** [Why this person gives you the most signal]
**What to watch for:** [The specific behavior or reaction that would tell you something important]

## Target user types (prioritized)

1. **[Type A]** — [Why priority 1]
2. **[Type B]** — [Why priority 2]
3. **[Type C]** — [Why priority 3]

## Outreach messages

### Warm network (direct reach)
Subject: [Subject if email / no subject for DM]

> [Message — personal, specific, short. Under 100 words.
> Name the specific problem. Name the specific ask.
> Not: "I'd love to get your thoughts." Yes: "Would you spend 20 minutes
> trying [specific thing] and telling me if [specific outcome] happened?"]

---

### Warm intro (referral request)
Subject: Quick intro request

> [Message to the person who can make the intro — what to say about you,
> why this person would benefit from talking to you]

---

### Cold outreach (if needed)
Subject: [Subject]

> [Shorter. More specific. Lead with the problem, not the product.
> "I'm building X for people who [specific pain]. Is that you?"
> Clear call to action — one specific ask.]

## The onboarding ask

When someone agrees to try it:

"I'd love to [format: watch you try it live / send you a link and ask 3 questions afterward].
Here is exactly what I want you to do: [specific task in specific context].
It should take about [X minutes]. After, I have 3 questions for you."

## Feedback capture

**Format:** [Live call / async written / async video]
**What to observe:** [Specific behaviors — where do they slow down, get confused, or light up]

**Three questions to ask every user:**
1. [Question 1 — about the core problem, not the product]
2. [Question 2 — about what they expected vs. what happened]
3. [Question 3 — would they use this again / tell someone about it?]

**The single most important thing to learn from user 1-10:**
[What specific signal would tell you whether you are on the right track]
```

## What makes good first-user outreach

**Bad:** "Hey, I'm building something for founders. Would love your feedback."

**Good:** "Hey Sarah — you mentioned on our call last month that you spend Sunday
nights assembling data for your investor updates. I built something to do that
automatically. Would you spend 20 minutes trying it on next week's update and
telling me if it saved you time? I'd be on the call with you."

The key elements:
- Reference something specific (from discovery or prior conversation)
- Name the problem explicitly
- Make the ask concrete and time-bounded
- Remove friction: you will be there, it will take 20 minutes

## The anti-patterns to avoid

- "Would love to get your thoughts" — too vague, easy to ignore
- Sending a Loom before offering a live call — live is better for learning
- Asking for feedback on the product before asking if the problem resonates
- Reaching out to important people first — risk of burning a bridge with a rough prototype
