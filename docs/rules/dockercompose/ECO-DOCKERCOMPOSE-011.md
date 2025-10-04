# ECO-DOCKERCOMPOSE-011: Use explicit build targets in Compose builds

**Tech:** docker-compose  
**Severity:** medium  
**Category:** efficiency  
**Confidence:** 0.7  
**Tags:** Flow

---

## Rationale
Not specifying target can ship dev stage by mistake.

## Detection
Detect 'build:' lacking 'target:'.

## Remediation
Add 'target:' for final runtime stage.

## KPI
- **Metric:** image_size_mb  
- **Estimated savings:** −10–40% size

## GoalOps Template
- **Goal:** Use explicit build targets in Compose builds  
- **Reality:** Current configuration violates this rule.  
- **Options:** Add 'target:' for final runtime stage.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `image_size_mb` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

