# ECO-SQLSERVER-004: Avoid WITH (NOLOCK) due to dirty reads

**Tech:** sqlserver  
**Severity:** medium  
**Category:** consistency  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
`NOLOCK` can return phantom/dirty rows and hide deadlocks while corrupting results.

## Detection
Detect `WITH (NOLOCK)` table hints.

## Remediation
Use proper isolation levels, read replicas, or snapshot isolation.

## KPI
- **Metric:** query_latency_ms  
- **Estimated savings:** −10–90% latency

## GoalOps Template
- **Goal:** Avoid WITH (NOLOCK) due to dirty reads  
- **Reality:** Current implementation violates this rule.  
- **Options:** Use proper isolation levels, read replicas, or snapshot isolation.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `query_latency_ms` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
