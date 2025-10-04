# ECO-SQLSERVER-003: Prefer DATETIME2 over DATETIME

**Tech:** sqlserver  
**Severity:** medium  
**Category:** governance  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
`DATETIME2` has larger range, higher precision, and better storage characteristics.

## Detection
Detect schema using `DATETIME`.

## Remediation
Migrate to `DATETIME2` where compatible.

## KPI
- **Metric:** query_latency_ms  
- **Estimated savings:** −10–90% latency

## GoalOps Template
- **Goal:** Prefer DATETIME2 over DATETIME  
- **Reality:** Current implementation violates this rule.  
- **Options:** Migrate to `DATETIME2` where compatible.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `query_latency_ms` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
