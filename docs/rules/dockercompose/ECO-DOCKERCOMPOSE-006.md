# ECO-DOCKERCOMPOSE-006: Mount secrets read-only

**Tech:** docker-compose  
**Severity:** high  
**Category:** security  
**Confidence:** 0.9  
**Tags:** Governance

---

## Rationale
Writable secrets risk tampering and leaks.

## Detection
Detect secret mounts lacking ':ro'.

## Remediation
Add ':ro' to secret mounts; use 'secrets:' feature.

## KPI
- **Metric:** incidents_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Mount secrets read-only  
- **Reality:** Current configuration violates this rule.  
- **Options:** Add ':ro' to secret mounts; use 'secrets:' feature.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `incidents_count` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

