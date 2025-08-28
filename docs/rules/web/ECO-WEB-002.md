# ECO-WEB-002: Unoptimized images (format/size)

**Tech:** web  
**Severity:** high  
**Category:** quick_win  
**Confidence:** 0.9  
**Tags:** Flow

---

## Rationale
Oversized raster images dominate transfer and decode energy.

## Detection
JPEG/PNG where WebP/AVIF possible; dims >> rendered size.

## Recommendation
Use responsive srcset, modern formats, pre-sized images.

## KPI
- **Metric:** image_bytes  
- **Estimated savings:** -40–90% bytes

## GoalOps Template
- **Goal:** Unoptimized images (format/size)  
- **Reality:** JPEG/PNG where WebP/AVIF possible; dims >> rendered size.  
- **Options:** Use responsive srcset, modern formats, pre-sized images.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `image_bytes` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

