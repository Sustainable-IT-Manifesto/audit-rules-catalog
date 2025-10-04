# ECO-TF-AZURE-014: Enable HTTP/2 and compression on App Service

**Tech:** terraform-azure  
**Severity:** low  
**Category:** efficiency  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
HTTP/2 and compression improve latency and reduce transfer size.

## Detection
Detect `azurerm_app_service` with `http2_enabled = false` or missing, or compression disabled in app settings.

## Remediation
Set `http2_enabled = true`; enable compression via app settings or reverse proxy.

## KPI
- **Metric:** ttfb_ms  
- **Estimated savings:** −5–20% TTFB / bytes

## GoalOps Template
- **Goal:** Enable HTTP/2 and compression on App Service  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Set `http2_enabled = true`; enable compression via app settings or reverse proxy.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `ttfb_ms` over a sprint.  
- **Three Ways Mapping:** Flow

---

