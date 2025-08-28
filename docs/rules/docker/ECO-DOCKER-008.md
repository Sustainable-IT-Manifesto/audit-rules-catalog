# ECO-DOCKER-008: Remove dev dependencies from runtime image

**Tech:** docker  
**Severity:** high  
**Category:** quick_win  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Dev deps add size and attack surface without runtime value.

## Detection
Node/Python build includes devDependencies/test tooling in final image.

## Recommendation
Use multi-stage or pip install --no-dev; npm ci --omit=dev for prod stage.

## KPI
- **Metric:** image_size_mb  
- **Estimated savings:** -20–50% size

## GoalOps Template
- **Goal:** Remove dev dependencies from runtime image  
- **Reality:** Node/Python build includes devDependencies/test tooling in final image.  
- **Options:** Use multi-stage or pip install --no-dev; npm ci --omit=dev for prod stage.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `image_size_mb` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

