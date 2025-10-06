# ECO-K8S-015: Avoid `:latest`; pin image tags and digests

**Tech:** kubernetes  
**Severity:** medium  
**Category:** governance  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Floating tags break reproducibility and rollback safety.

## Detection
Detect container images without explicit tag/digest.

## Remediation
Use version tags and digests.

## KPI
- **Metric:** change_failure_rate  
- **Estimated savings:** Lower CFR

## GoalOps Template
- **Goal:** Avoid `:latest`; pin image tags and digests  
- **Reality:** Current manifests don’t comply.  
- **Options:** Use version tags and digests.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `change_failure_rate` over a sprint.  
- **Three Ways Mapping:** Flow

---
