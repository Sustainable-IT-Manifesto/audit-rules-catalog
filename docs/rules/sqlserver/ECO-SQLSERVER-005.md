# ECO-SQLSERVER-005: TOP without ORDER BY yields non-deterministic results

**Tech:** sqlserver  
**Severity:** medium  
**Category:** efficiency  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Without ordering, TOP N returns arbitrary rows depending on plan.

## Detection
Detect `SELECT TOP (N)` without `ORDER BY`.

## Remediation
Always specify ORDER BY with TOP.

## KPI
- **Metric:** query_latency_ms  
- **Estimated savings:** −10–90% latency

## GoalOps Template
- **Goal:** TOP without ORDER BY yields non-deterministic results  
- **Reality:** Current implementation violates this rule.  
- **Options:** Always specify ORDER BY with TOP.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `query_latency_ms` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
