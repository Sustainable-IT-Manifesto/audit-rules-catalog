# ECO-DOCKERCOMPOSE-003: Set restart policies for resilience

**Tech:** docker-compose  
**Severity:** medium  
**Category:** reliability  
**Confidence:** 0.8  
**Tags:** Feedback

---

## Rationale
Restart policies reduce downtime for transient failures.

## Detection
Detect services without 'restart:'.

## Remediation
Add 'restart: unless-stopped' or similar.

## KPI
- **Metric:** uptime_percent  
- **Estimated savings:** +0.1–0.5 pts

## GoalOps Template
- **Goal:** Set restart policies for resilience  
- **Reality:** Current configuration violates this rule.  
- **Options:** Add 'restart: unless-stopped' or similar.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `uptime_percent` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

