# ECO-DOCKERCOMPOSE-005: Configure log rotation

**Tech:** docker-compose  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Unbounded logs fill disks and waste IO.

## Detection
Detect missing 'logging.options' with 'max-size'/'max-file'.

## Remediation
Add log driver/options with rotation caps.

## KPI
- **Metric:** storage_used_mb  
- **Estimated savings:** −5–30% storage

## GoalOps Template
- **Goal:** Configure log rotation  
- **Reality:** Current configuration violates this rule.  
- **Options:** Add log driver/options with rotation caps.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `storage_used_mb` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

