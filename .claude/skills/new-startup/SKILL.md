---
name: new-startup
description: Onboard a new startup. Creates work/startup-N/ with all skill folders, sets it as the active startup, and captures the founder's initial context. Run this before any other skill.
---

# New Startup Onboarding

Sets up a fresh workspace for a new startup and makes it the active one.
Run this once per startup, before invoking any other skill.

## Steps

1. **Find the next startup number**

   Scan `work/` for directories matching `startup-N` (e.g., `startup-1`, `startup-2`).
   The new startup is `startup-N+1`. If no startup directories exist yet, use `startup-1`.

2. **Create the workspace**

   Create `work/startup-N/` with subdirectories for every skill:
   ```
   work/startup-N/
     founder-opportunity-map/
     customer-discovery-synthesizer/
     synthetic-customer-panel/
     product-strategy-brief/
     prototype-scope/
     prototype-review/
     first-users-outreach/
     pmf-signal-review/
     growth-experiment-backlog/
     founder-hiring-scorecard/
     fundraising-narrative/
     demo-day-script/
     weekly-founder-review/
   ```

3. **Set as active**

   Write `startup-N` (just the directory name, no path) to `work/.current`.

4. **Capture founder context**

   Ask the founder these questions one at a time. Do not ask them all at once.

   - "What's the startup about — one sentence, rough is fine."
   - "What stage are you at? (idea, early customers, post-revenue, other)"
   - "What's your background — what do you know really well that most people don't?"
   - "What do you want to figure out first — the problem, the customer, the product, or something else?"

   Their answers do not need to be polished. Write them as-is into
   `work/startup-N/founder-opportunity-map/founder-context.md` using the format below.

5. **Confirm and suggest the first skill**

   Tell the founder:
   - Their workspace is at `work/startup-N/`
   - It is now the active startup (`work/.current` is updated)
   - Based on their answer to "what do you want to figure out first," suggest the right skill to run next

## founder-context.md format

```markdown
# Founder Context — [startup-N]

*Created: [date]*

## The startup
[Their one-sentence answer]

## Stage
[Their answer]

## Background / domain expertise
[Their answer]

## What to figure out first
[Their answer]

---
*Drop additional notes, transcripts, or observations anywhere in this file.
Skills are designed to work from rough input.*
```

## Suggesting the next skill

| If they want to figure out... | Suggest |
|-------------------------------|---------|
| The problem / what to work on | `/founder-opportunity-map` |
| The customer / who to talk to | `/customer-discovery-synthesizer` |
| Whether the idea is any good | `/synthetic-customer-panel` |
| What to build | `/product-strategy-brief` |
| Where they are in the journey | `/weekly-founder-review` |

If unclear, default to `/founder-opportunity-map` — it works from any starting point.

## Error handling

If `work/` does not exist: create it, then proceed.

If `work/.current` already points to a startup and the founder did not explicitly
say they are starting something new: confirm before creating a new startup directory.
Say: "You have an active startup at `work/[current]`. Start a new one anyway?"
