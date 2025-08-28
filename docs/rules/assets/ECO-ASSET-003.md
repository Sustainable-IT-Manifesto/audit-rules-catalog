# ECO-ASSET-003: Video autoplay or high bitrate by default

**Tech:** assets  
**Severity:** medium  
**Category:** governance  
**Confidence:** 0.7  
**Tags:** Flow

---

## Rationale
Autoplay and high bitrate waste client energy/data.

## Detection
Autoplay enabled; >1080p on mobile; no adaptive bitrate.

## Recommendation
Disable autoplay; use ABR; reduce default resolution.

## KPI
- **Metric:** video_bytes  
- **Estimated savings:** -30–70% bytes

## GoalOps Template
- **Goal:** Video autoplay or high bitrate by default  
- **Reality:** Autoplay enabled; >1080p on mobile; no adaptive bitrate.  
- **Options:** Disable autoplay; use ABR; reduce default resolution.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `video_bytes` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

