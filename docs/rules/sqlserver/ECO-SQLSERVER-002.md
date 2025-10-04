# ECO-SQLSERVER-002: Parameterize queries to avoid SQL injection and improve plan cache

**Tech:** sqlserver  
**Severity:** high  
**Category:** security  
**Confidence:** 0.8  
**Tags:** Governance

---

## Rationale
String-concatenated SQL risks injection and prevents plan caching.

## Detection
Detect concatenated SQL fragments with variables.

## Remediation
Use placeholders/prepared statements from the DB driver/ORM.

## KPI
- **Metric:** query_latency_ms  
- **Estimated savings:** −10–90% latency

## GoalOps Template
- **Goal:** Parameterize queries to avoid SQL injection and improve plan cache  
- **Reality:** Current implementation violates this rule.  
- **Options:** Use placeholders/prepared statements from the DB driver/ORM.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `query_latency_ms` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---
