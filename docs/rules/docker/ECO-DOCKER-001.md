# ECO-DOCKER-001: Use multi-stage builds to slim images

**Tech:** docker  
**Severity:** high  
**Category:** quick_win  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Single-stage images bake dev tooling and artifacts into runtime images, increasing pull time and compute.

## Detection
Dockerfile lacks multiple FROM stages; build tools present in final image.

## Recommendation
Refactor to multi-stage; copy only runtime artifacts to final stage.

## KPI
- **Metric:** image_size_mb  
- **Estimated savings:** -40–70% image size

## GoalOps Template
- **Goal:** Use multi-stage builds to slim images  
- **Reality:** Dockerfile lacks multiple FROM stages; build tools present in final image.  
- **Options:** Refactor to multi-stage; copy only runtime artifacts to final stage.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `image_size_mb` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

