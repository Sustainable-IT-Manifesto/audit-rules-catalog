# ECO-K8S-031: Kubernetes best-practice compliance

**Tech:** kubernetes  
**Severity:** medium  
**Category:** governance  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Detector flags common anti‑patterns vs PSS and best practices.

## Detection
Scan YAML/templates for violations.

## Remediation
Apply recommended fields and policies.

## KPI
- **Metric:** defect_rate  
- **Estimated savings:** Lower CFR

## GoalOps Template
- **Goal:** Kubernetes best-practice compliance  
- **Reality:** Current manifests don’t comply.  
- **Options:** Apply recommended fields and policies.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `defect_rate` over a sprint.  
- **Three Ways Mapping:** Flow

---
