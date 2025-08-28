# ECO-CI-001: Redundant matrix jobs or duplicate workflows

**Tech:** ci  
**Severity:** medium  
**Category:** governance  
**Confidence:** 0.75  
**Tags:** Flow

---

## Rationale
Unnecessary parallel jobs multiply CI compute.

## Detection
Matrix includes identical environments; overlapping triggers.

## Recommendation
Deduplicate; conditional matrix; path filters.

## KPI
- **Metric:** ci_vcpu_minutes  
- **Estimated savings:** -20–50% minutes

## GoalOps Template
- **Goal:** Redundant matrix jobs or duplicate workflows  
- **Reality:** Matrix includes identical environments; overlapping triggers.  
- **Options:** Deduplicate; conditional matrix; path filters.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `ci_vcpu_minutes` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

