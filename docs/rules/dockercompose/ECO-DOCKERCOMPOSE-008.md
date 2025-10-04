# ECO-DOCKERCOMPOSE-008: Avoid bind-mounting database data directories

**Tech:** docker-compose  
**Severity:** medium  
**Category:** reliability  
**Confidence:** 0.7  
**Tags:** Feedback

---

## Rationale
Bind mounts risk corruption and OS-specific perms.

## Detection
Detect mounts into /var/lib/(mysql|postgresql) etc.

## Remediation
Use named volumes with proper backup/restore.

## KPI
- **Metric:** incidents_count  
- **Estimated savings:** Lower risk

## GoalOps Template
- **Goal:** Avoid bind-mounting database data directories  
- **Reality:** Current configuration violates this rule.  
- **Options:** Use named volumes with proper backup/restore.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `incidents_count` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

