---
id: as-applied-data-auto-ingestible
type: assumption
source: product-strategy-brief
created: 2026-06-14
startup: startup-2
confidence: low
status: active
tags:
  - technical-feasibility
  - data
  - adoption
---

# As-applied and field-history data can be auto-ingested from the tools consultants/farmers already use, with minimal manual entry

**Validation status:** unvalidated
"Every farmer app dies on data entry." For AgroGuard to become a load-bearing weekly habit,
spray records and field history must flow in automatically from existing equipment/software
(e.g., FieldView, John Deere Operations Center, sprayer controllers, co-op platforms) rather
than being typed in.

**What "validated" looks like:** A technical spike successfully pulls real as-applied records
from at least one or two common systems via export/API with little manual cleanup.
**What "invalidated" looks like:** Data is locked in proprietary silos, requires manual export
per field, or is too messy/inconsistent to use without heavy hand-entry.
**How we'll test it:** Technical spike against real data exports before committing to a build.
**Current evidence:** Identified as a hard requirement in [[ag-software-dies-on-data-entry]]
(from simulated interviews). Feasibility unknown.
