# ECO-ASSET-001: Deduplicate identical images/fonts

**Tech:** assets  
**Severity:** low  
**Category:** quick_win  
**Confidence:** 0.7  
**Tags:** Flow

---

## Rationale
Duplicate assets inflate bundles and storage.

## Detection
Hash-colliding assets in repo or build output.

## Recommendation
Deduplicate; reference single copy; use asset pipeline.

## KPI
- **Metric:** asset_bytes  
- **Estimated savings:** -10–30% bytes

## GoalOps Template
- **Goal:** Deduplicate identical images/fonts  
- **Reality:** Hash-colliding assets in repo or build output.  
- **Options:** Deduplicate; reference single copy; use asset pipeline.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `asset_bytes` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

