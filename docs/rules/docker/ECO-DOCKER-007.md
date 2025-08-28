# ECO-DOCKER-007: Minimize layers with COPY --chown and targeted paths

**Tech:** docker  
**Severity:** low  
**Category:** quick_win  
**Confidence:** 0.6  
**Tags:** Flow

---

## Rationale
Copying entire contexts inflates layers and rebuild scope.

## Detection
COPY . . patterns without .dockerignore; ownership fixes via separate RUN.

## Recommendation
Copy only required directories; use --chown directly in COPY.

## KPI
- **Metric:** image_layers  
- **Estimated savings:** -10–25% layers

## GoalOps Template
- **Goal:** Minimize layers with COPY --chown and targeted paths  
- **Reality:** COPY . . patterns without .dockerignore; ownership fixes via separate RUN.  
- **Options:** Copy only required directories; use --chown directly in COPY.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `image_layers` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

