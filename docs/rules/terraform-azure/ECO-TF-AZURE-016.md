# ECO-TF-AZURE-016: Enable Cosmos DB autoscale throughput

**Tech:** terraform-azure  
**Severity:** medium  
**Category:** cost_control  
**Confidence:** 0.85  
**Tags:** Flow

---

## Rationale
Autoscale RUs prevent over-provisioning and throttling.

## Detection
Detect `azurerm_cosmosdb_account`/`_sql_database`/`_container` without autoscale throughput settings.

## Remediation
Enable autoscale (e.g., `max_throughput`) and right-size per workload patterns.

## KPI
- **Metric:** cosmos_ru_usd  
- **Estimated savings:** −15–50% RU spend

## GoalOps Template
- **Goal:** Enable Cosmos DB autoscale throughput  
- **Reality:** Current Terraform doesn’t comply.  
- **Options:** Enable autoscale (e.g., `max_throughput`) and right-size per workload patterns.  
- **Will:** Assign owner, sprint, and deadline.  
- **SMARTer:** Track `cosmos_ru_usd` over a sprint.  
- **Three Ways Mapping:** Flow

---

