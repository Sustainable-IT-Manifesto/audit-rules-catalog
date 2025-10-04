# ECO-DOCKER-016: Order COPY to maximize layer caching (copy lockfiles first)

**Tech:** docker  
**Severity:** medium  
**Category:** best_practice  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Copying full source before deps invalidates cache on every change.

## Detection
Detect COPY . before copying lockfiles/requirements.

## Remediation
COPY lockfiles/requirements first, run install, then COPY .

## KPI
- **Metric:** build_time_sec  
- **Estimated savings:** −20–50% time

## GoalOps Template
- **Goal:** Order COPY to maximize layer caching (copy lockfiles first)  
- **Reality:** Current configuration violates this rule.  
- **Options:** COPY lockfiles/requirements first, run install, then COPY .  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `build_time_sec` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

