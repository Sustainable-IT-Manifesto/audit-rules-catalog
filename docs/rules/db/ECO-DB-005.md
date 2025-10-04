# ECO-DB-005: Avoid huge IN(...) lists

**Tech:** database  
**Severity:** medium  
**Category:** efficiency  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Large `IN` lists inflate planning time and can exceed parameter limits.

## Detection
Detect `IN` lists with many literals.

## Remediation
Use temporary tables, JOINs, or array parameters.

## KPI
- **Metric:** query_latency_ms  
- **Estimated savings:** −10–90% latency

## GoalOps Template
- **Goal:** Avoid huge IN(...) lists  
- **Reality:** Current implementation violates this rule.  
- **Options:** Use temporary tables, JOINs, or array parameters.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `query_latency_ms` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
