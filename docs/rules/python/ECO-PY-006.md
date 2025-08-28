# ECO-PY-006: Inefficient logging in hot paths

**Tech:** python  
**Severity:** low  
**Category:** quick_win  
**Confidence:** 0.6  
**Tags:** Flow

---

## Rationale
String formatting and IO in tight loops adds overhead.

## Detection
f-strings evaluated before log level check; many debug logs.

## Recommendation
Use lazy logging; guard by level; batch logs.

## KPI
- **Metric:** cpu_seconds  
- **Estimated savings:** -5–15% CPU

## GoalOps Template
- **Goal:** Inefficient logging in hot paths  
- **Reality:** f-strings evaluated before log level check; many debug logs.  
- **Options:** Use lazy logging; guard by level; batch logs.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `cpu_seconds` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

