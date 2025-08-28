# ECO-PY-004: Over-precision or unnecessary Decimal use

**Tech:** python  
**Severity:** low  
**Category:** quick_win  
**Confidence:** 0.5  
**Tags:** Flow

---

## Rationale
High precision math is slower and energy-costly when not needed.

## Detection
Decimal in hot paths without financial need; float64 where float32 OK.

## Recommendation
Use floats/NumPy dtypes appropriate to domain.

## KPI
- **Metric:** cpu_seconds  
- **Estimated savings:** -5–20% CPU

## GoalOps Template
- **Goal:** Over-precision or unnecessary Decimal use  
- **Reality:** Decimal in hot paths without financial need; float64 where float32 OK.  
- **Options:** Use floats/NumPy dtypes appropriate to domain.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `cpu_seconds` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

