# ECO-PY-001: Inefficient loops / avoid repeated work

**Tech:** python  
**Severity:** medium  
**Category:** quick_win  
**Confidence:** 0.7  
**Tags:** Flow

---

## Rationale
Python loops with repeated computation inflate CPU time.

## Detection
Repeated regex compilation, function calls, or attribute lookups inside loops.

## Recommendation
Hoist invariants; precompile regex; use comprehensions/vectorize.

## KPI
- **Metric:** cpu_seconds  
- **Estimated savings:** -10–40% CPU

## GoalOps Template
- **Goal:** Inefficient loops / avoid repeated work  
- **Reality:** Repeated regex compilation, function calls, or attribute lookups inside loops.  
- **Options:** Hoist invariants; precompile regex; use comprehensions/vectorize.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `cpu_seconds` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

