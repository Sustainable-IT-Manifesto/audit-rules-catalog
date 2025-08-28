# ECO-DOCKER-010: Prefer COPY over ADD (except for archives/URLs)

**Tech:** docker  
**Severity:** low  
**Category:** governance  
**Confidence:** 0.6  
**Tags:** Flow

---

## Rationale
ADD has implicit behaviors that enlarge layers unexpectedly.

## Detection
ADD used for local files where COPY suffices.

## Recommendation
Replace ADD with COPY; keep ADD for verified tar/URL needs.

## KPI
- **Metric:** image_layers  
- **Estimated savings:** -5–10% layers

## GoalOps Template
- **Goal:** Prefer COPY over ADD (except for archives/URLs)  
- **Reality:** ADD used for local files where COPY suffices.  
- **Options:** Replace ADD with COPY; keep ADD for verified tar/URL needs.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `image_layers` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

