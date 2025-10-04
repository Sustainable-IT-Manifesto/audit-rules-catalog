# ECO-DOCKER-017: Use requirements.txt or pinned constraints for pip

**Tech:** docker  
**Severity:** medium  
**Category:** governance  
**Confidence:** 0.8  
**Tags:** Feedback

---

## Rationale
Unpinned deps reduce reproducibility.

## Detection
Detect 'pip install <pkg>' w/out '==' or requirements file.

## Remediation
Install via requirements.txt with pinned versions.

## KPI
- **Metric:** rollbacks_hours  
- **Estimated savings:** −20–40% MTTR

## GoalOps Template
- **Goal:** Use requirements.txt or pinned constraints for pip  
- **Reality:** Current configuration violates this rule.  
- **Options:** Install via requirements.txt with pinned versions.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `rollbacks_hours` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

