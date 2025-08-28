# ECO-CI-003: Artifact retention too long

**Tech:** ci  
**Severity:** low  
**Category:** governance  
**Confidence:** 0.7  
**Tags:** Flow

---

## Rationale
Long-lived artifacts consume storage.

## Detection
Artifacts kept >14 days without need.

## Recommendation
Reduce retention; compress artifacts; avoid large artifacts.

## KPI
- **Metric:** artifact_gb_month  
- **Estimated savings:** -30–80% GB

## GoalOps Template
- **Goal:** Artifact retention too long  
- **Reality:** Artifacts kept >14 days without need.  
- **Options:** Reduce retention; compress artifacts; avoid large artifacts.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `artifact_gb_month` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

