# ECO-DOCKER-014: Use 'npm ci' in CI for reproducible installs

**Tech:** docker  
**Severity:** low  
**Category:** efficiency  
**Confidence:** 0.7  
**Tags:** Flow

---

## Rationale
npm install may mutate lockfiles and be slower.

## Detection
Detect 'npm install' where package-lock.json exists.

## Remediation
Switch to 'npm ci' in build stage.

## KPI
- **Metric:** build_time_sec  
- **Estimated savings:** −10–30% time

## GoalOps Template
- **Goal:** Use 'npm ci' in CI for reproducible installs  
- **Reality:** Current configuration violates this rule.  
- **Options:** Switch to 'npm ci' in build stage.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `build_time_sec` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

