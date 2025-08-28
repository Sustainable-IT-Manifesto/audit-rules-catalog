# ECO-CI-004: Run tests selectively (changed paths)

**Tech:** ci  
**Severity:** medium  
**Category:** deep_work  
**Confidence:** 0.65  
**Tags:** Flow

---

## Rationale
Running all tests on every change wastes compute.

## Detection
No path-based test selection; no impacted tests.

## Recommendation
Adopt test impact analysis or path filters; split smoke vs full.

## KPI
- **Metric:** ci_vcpu_minutes  
- **Estimated savings:** -20–60% minutes

## GoalOps Template
- **Goal:** Run tests selectively (changed paths)  
- **Reality:** No path-based test selection; no impacted tests.  
- **Options:** Adopt test impact analysis or path filters; split smoke vs full.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `ci_vcpu_minutes` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

