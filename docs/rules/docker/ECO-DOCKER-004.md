# ECO-DOCKER-004: Do not run as root

**Tech:** docker  
**Severity:** low  
**Category:** governance  
**Confidence:** 0.8  
**Tags:** Governance

---

## Rationale
Root containers require stronger isolation and hinder multitenant efficiency.

## Detection
USER not set or set to root in final stage.

## Recommendation
Create non-root user and set USER; fix file ownerships.

## KPI
- **Metric:** non_root_percentage  
- **Estimated savings:** ≥95% workloads non-root

## GoalOps Template
- **Goal:** Do not run as root  
- **Reality:** USER not set or set to root in final stage.  
- **Options:** Create non-root user and set USER; fix file ownerships.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `non_root_percentage` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Governance

---

