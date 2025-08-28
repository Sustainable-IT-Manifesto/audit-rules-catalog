# ECO-DOCKER-002: Switch to smaller base image (e.g., alpine, distroless)

**Tech:** docker  
**Severity:** medium  
**Category:** quick_win  
**Confidence:** 0.7  
**Tags:** Flow

---

## Rationale
Large base images waste storage, bandwidth, and cold-start time.

## Detection
Base image in FROM is debian/ubuntu where alpine/distroless equivalent exists.

## Recommendation
Use minimal base images when compatible; evaluate glibc/musl needs.

## KPI
- **Metric:** image_size_mb  
- **Estimated savings:** -20–60% image size

## GoalOps Template
- **Goal:** Switch to smaller base image (e.g., alpine, distroless)  
- **Reality:** Base image in FROM is debian/ubuntu where alpine/distroless equivalent exists.  
- **Options:** Use minimal base images when compatible; evaluate glibc/musl needs.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `image_size_mb` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

