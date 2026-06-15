# Prototype Scope
*Generated: 2026-06-14 | Time budget: ~half a day (3–4 hrs Claude Code)*

> **Provenance:** Derived from `strategy-brief.md`, which is built on illustrative sample
> discovery. This prototype exists to produce something concrete enough to put in front of a
> *real* crop consultant and test the paid-pilot question.

## The riskiest assumption being tested
That a real independent crop consultant will **trust an explainable, AI-generated resistance
recommendation enough to sign their name to it** — the necessary precondition for the deeper
business risk (will they pay a pilot fee?). If the recommendation isn't sign-worthy, the
willingness-to-pay question never even gets a fair test.

> Note: WTP itself can only be tested in a real sales conversation. The prototype's job is to
> make the value real enough that that conversation is worth having. It tests *trust/quality*;
> the buyer-discovery guide tests *dollars*.

## The one job
Take a field's spray history and current weed pressure and produce an explainable,
resistance-aware spray program recommendation that a crop consultant would sign.

## Inputs
A pasted/structured record for 1–3 fields:
- Crop + region (e.g., "soybeans, west-central Iowa")
- Last 2–3 seasons of applications: product/active ingredient + herbicide **mode-of-action
  (MoA / WSSA group) number** + timing
- Known resistant weeds on the field (e.g., "PPO-resistant waterhemp")
- Current scouting / weed pressure note

*(v0 uses hand-entered or pasted data on purpose — see out-of-scope.)*

## Outputs
A per-field recommendation the consultant can review and edit:
- Recommended program: products, rates, timing, tank-mix
- **Explicit MoA-rotation reasoning** — which groups, why, in plain language
- **Resistance-stewardship warnings** — e.g., "Group 15 used 3 passes running on this field;
  rotating off it this pass to slow selection pressure"
- A short, editable rationale paragraph written so the consultant could send/sign it as-is

## In scope (v0)
- The core reasoning: history + weed pressure → resistance-aware program
- A baked-in herbicide MoA / WSSA group knowledge base (group classifications + resistance logic)
- Mode-of-action stacking detection and a clear warning when a program over-relies on one group
- Plain-language, explainable rationale (the trust-maker — this is the whole point)
- Run cleanly on 2–3 real test fields with expert-checkable output

## Explicitly out of scope
| Out of scope | Why |
|-------------|-----|
| Auto-ingesting as-applied data from FieldView/Ops Center | Separate technical assumption; manual input is fine to test *trust* |
| Multi-grower portfolio dashboard / "more acres" capacity story | Doesn't test the riskiest assumption; adds UI complexity |
| Logistics / spray sequencing across acres | Different product and customer (large operators) |
| Co-op enterprise features, knowledge-capture | Expansion, not beachhead |
| Farmer-facing UI | We build for the consultant; farmer buys the person |
| Insecticides / fungicides | Focus on herbicide/weed resistance — the sharpest pain |
| Legal label-compliance certification | High complexity, doesn't test trust; consultant still reviews |

## Success criteria

**The prototype works if:**
On 2–3 real test fields, it produces recommendations that (a) rotate modes of action correctly,
(b) catch the stacking/resistance risk an expert would catch, and (c) explain the reasoning so
clearly that a real consultant, shown the output, says "yes, I'd sign that." The real-world bar
on top: that consultant agrees to a paid pilot.

**The prototype fails if:**
The recommendations are agronomically wrong, the reasoning is a black box the consultant won't
trust, it needs so much hand-holding/data entry to run that it's useless, or consultants say
"neat" but won't put their name on it.

## Build time budget
~3–4 hours of Claude Code time. The prototype **is** an AI behavior (resistance reasoning +
explainable output), so it builds fast as a Claude skill. Leave buffer — first pass won't be done.

## Readiness checklist

Before opening `https://github.com/sinned/prototype-with-claude`:
- [x] Product brief is written and reviewed
- [x] Riskiest assumption is clearly stated
- [x] The one job can be stated in one sentence
- [ ] **At least one real test case exists** (real field history → expert-expected recommendation)
      — ⚠️ this is the gap. You need at least one real or expert-validated field example, or the
      output can't be judged for correctness.
- [x] Time budget is set and committed

## Handoff to the build environment

### Path B: AI behavior prototype (use prototype-with-claude) — RECOMMENDED

The prototype is fundamentally an AI behavior, so go this route:

1. Open `https://github.com/sinned/prototype-with-claude` in Claude Code.
2. Run `/new-skill` — paste the **one job** and **success criteria** from this document, plus
   the input/output formats above.
3. Provide the herbicide MoA / WSSA group reference as the skill's domain knowledge.
4. Run `/eval-skill` against your real test field(s).
5. Run `/improve-skill` to fix any agronomically wrong or unexplainable outputs.
6. Return here and run `/prototype-review`.

### Path A: Full product feature (use gstack)
Only if you decide to wrap this in a real app with data ingestion (a v1 concern, not now). If
so: `/office-hours` (paste the one-job line) → `/autoplan` → build → `/review` → `/qa` → `/ship`.

## The one thing to do before building
Get **one real, expert-validated field example** (real spray history + the program a good
agronomist would actually recommend). Without it, you can build the behavior but you can't tell
if it's *right* — and "right" is the entire trust bet. This is also a perfect first ask in a
buyer-discovery call: "Walk me through a real field and what you'd recommend."
