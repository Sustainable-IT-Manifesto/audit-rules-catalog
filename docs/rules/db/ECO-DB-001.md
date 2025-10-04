# ECO-DB-001: Use half-open date ranges instead of BETWEEN on timestamps

**Tech:** database  
**Severity:** medium  
**Category:** efficiency  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
`BETWEEN` is inclusive and can duplicate boundaries; time zones add subtle bugs.

## Detection
Detect `BETWEEN` on TIMESTAMP/DATETIME columns.

## Remediation
Use `>= start AND < end` with normalized timezones.

## KPI
- **Metric:** query_latency_ms  
- **Estimated savings:** −10–90% latency

## GoalOps Template
- **Goal:** Use half-open date ranges instead of BETWEEN on timestamps  
- **Reality:** Current implementation violates this rule.  
- **Options:** Use `>= start AND < end` with normalized timezones.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `query_latency_ms` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
