# ECO-DOCKERCOMPOSE-010: Avoid legacy 'links' in Compose

**Tech:** docker-compose  
**Severity:** low  
**Category:** maintainability  
**Confidence:** 0.6  
**Tags:** Flow

---

## Rationale
Links are deprecated and brittle vs networks/service names.

## Detection
Detect 'links:' usage.

## Remediation
Use default networks and service names for discovery.

## KPI
- **Metric:** change_failure_rate  
- **Estimated savings:** Lower CFR

## GoalOps Template
- **Goal:** Avoid legacy 'links' in Compose  
- **Reality:** Current configuration violates this rule.  
- **Options:** Use default networks and service names for discovery.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `change_failure_rate` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

