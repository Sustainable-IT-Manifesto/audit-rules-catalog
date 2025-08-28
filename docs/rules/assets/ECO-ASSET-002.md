# ECO-ASSET-002: Subsetting & compressing web fonts

**Tech:** assets  
**Severity:** medium  
**Category:** deep_work  
**Confidence:** 0.8  
**Tags:** Flow

---

## Rationale
Full font families add 100s of KB per page.

## Detection
Multiple full fonts loaded; no unicode-range subsetting.

## Recommendation
Subset to needed glyphs; use WOFF2; preload wisely.

## KPI
- **Metric:** font_bytes  
- **Estimated savings:** -40–80% bytes

## GoalOps Template
- **Goal:** Subsetting & compressing web fonts  
- **Reality:** Multiple full fonts loaded; no unicode-range subsetting.  
- **Options:** Subset to needed glyphs; use WOFF2; preload wisely.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `font_bytes` for improvement, time-bound within sprint.  
- **Three Ways Mapping:** Flow

---

