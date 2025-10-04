# ECO-DOCKERCOMPOSE-007: Avoid mounting entire repo as a bind volume

**Tech:** docker-compose  
**Severity:** low  
**Category:** efficiency  
**Confidence:** 0.6  
**Tags:** Flow

---

## Rationale
Mounting the whole repo can slow IO and leak files.

## Detection
Detect 'volumes: - .:' root binds.

## Remediation
Bind only needed subpaths; use .dockerignore for context.

## KPI
- **Metric:** io_wait_ms  
- **Estimated savings:** −5–25% IO

## GoalOps Template
- **Goal:** Avoid mounting entire repo as a bind volume  
- **Reality:** Current configuration violates this rule.  
- **Options:** Bind only needed subpaths; use .dockerignore for context.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `io_wait_ms` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

