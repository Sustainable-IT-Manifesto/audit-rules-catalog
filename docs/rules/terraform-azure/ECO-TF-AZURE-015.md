# ECO-TF-AZURE-015: Use Azure SQL Serverless with autopause where feasible

**Tech:** terraform-azure  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Auto-pause saves cost for spiky/idle workloads.

## Detection
Detect `azurerm_mssql_database` not using `sku_name` serverless tiers or missing `auto_pause_delay`.

## Remediation
Adopt Serverless SKUs with `auto_pause_delay` tuned to workload.

## KPI
- **Metric:** sql_monthly_usd  
- **Estimated savings:** −20–60% DB cost

## GoalOps Template
- **Goal:** Use Azure SQL Serverless with autopause where feasible  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Adopt Serverless SKUs with `auto_pause_delay` tuned to workload.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `sql_monthly_usd` over a sprint.  
- **Three Ways Mapping:** Flow

---

