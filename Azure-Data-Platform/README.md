
# 🚀 Project 1: Azure Data Platform for Fleet & Financial Reporting

## 📌 README.md

### Overview

End-to-end Azure data platform designed to consolidate fleet operational data and financial metrics into a unified analytics layer for executive reporting.

### Business Problem

* Fragmented on-prem SQL Server systems
* Manual reporting cycles and inconsistent KPIs
* Slow access to operational and financial insights

### Solution Summary

* Automated ingestion from on-prem SQL Server using Azure Data Factory
* Lakehouse architecture on ADLS Gen2 (Raw → Curated → Analytics)
* Transformations using Azure Databricks (Python & SQL)
* Power BI dashboards built on Synapse semantic models

### Business Impact

* Fleet utilization improved to **85.6%**
* Downtime reduced to **320 hours**
* Reporting turnaround reduced from **45 hours to <10 hours**
* Financial reporting standardized in **ZAR**

---

## 🏗️ Architecture Diagram (Description)

**Flow:**

1. On‑Prem SQL Server → Azure Data Factory (Self‑Hosted IR)
2. ADLS Gen2 – Raw Zone (Parquet)
3. Databricks – Cleansing, joins, business rules
4. ADLS Gen2 – Curated & Analytics Zones
5. Azure Synapse – External tables & views
6. Power BI – Executive dashboards

*(Diagram labels: Security via Azure AD, Secrets via Key Vault)*

---

## 🔧 Pipeline & Script Logic

### ADF

* Full & incremental extraction using watermark on `LastUpdatedDate`
* Parameterized pipelines for reusability

### Databricks

* Schema enforcement
* Fleet KPIs (utilization %, downtime hours)
* Financial aggregations by period

---

## 📄 Governance & Security

* Azure AD RBAC
* Data access by zone (Raw restricted)
* Audit logging enabled

---



