# ECO-DOCKER-012: Clean package manager caches after install

**Tech:** docker  
**Severity:** medium  
**Category:** waste_reduction  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Leftover caches increase layer size and transfer time.

## Detection
Detect apt/pip installs without subsequent cache clean.

## Remediation
Add 'rm -rf /var/lib/apt/lists/*' and pip cache purge steps.

## KPI
- **Metric:** image_size_mb  
- **Estimated savings:** −5–20% size

## GoalOps Template
- **Goal:** Clean package manager caches after install  
- **Reality:** Current configuration violates this rule.  
- **Options:** Add 'rm -rf /var/lib/apt/lists/*' and pip cache purge steps.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `image_size_mb` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

