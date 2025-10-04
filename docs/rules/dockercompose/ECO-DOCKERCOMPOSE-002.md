# ECO-DOCKERCOMPOSE-002: Avoid privileged containers

**Tech:** docker-compose  
**Severity:** high  
**Category:** security  
**Confidence:** 0.9  
**Tags:** Governance

---

## Rationale
privileged: true grants near-host root access.

## Detection
Detect 'privileged: true'.

## Remediation
Remove privileged; use specific capabilities as needed.

## KPI
- **Metric:** incidents_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Avoid privileged containers  
- **Reality:** Current configuration violates this rule.  
- **Options:** Remove privileged; use specific capabilities as needed.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `incidents_count` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

