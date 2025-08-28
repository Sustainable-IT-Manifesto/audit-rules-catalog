# ECO-K8S-004: Use lean base images for sidecars

**Tech:** kubernetes  
**Severity:** low  
**Category:** quick_win  
**Confidence:** 0.65  
**Tags:** Flow

---

## Rationale
Sidecars often run 24/7; heavy images multiply waste.

## Detection
Sidecars using generic heavy images.

## Recommendation
Switch to minimal images; consolidate sidecars where feasible.

## KPI
- **Metric:** image_size_mb  
- **Estimated savings:** -20–50% sidecar size

## GoalOps Template
- **Goal:** Use lean base images for sidecars  
- **Reality:** Sidecars using generic heavy images.  
- **Options:** Switch to minimal images; consolidate sidecars where feasible.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `image_size_mb` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

