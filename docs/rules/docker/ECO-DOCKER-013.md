# ECO-DOCKER-013: Use '--no-install-recommends' with apt-get

**Tech:** docker  
**Severity:** low  
**Category:** efficiency  
**Confidence:** 0.7  
**Tags:** Flow

---

## Rationale
Recommends pull unnecessary packages inflating images.

## Detection
Find 'apt-get install' lacking '--no-install-recommends'.

## Remediation
Add '--no-install-recommends' and explicitly list needed deps.

## KPI
- **Metric:** image_size_mb  
- **Estimated savings:** −5–15% size

## GoalOps Template
- **Goal:** Use '--no-install-recommends' with apt-get  
- **Reality:** Current configuration violates this rule.  
- **Options:** Add '--no-install-recommends' and explicitly list needed deps.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `image_size_mb` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

