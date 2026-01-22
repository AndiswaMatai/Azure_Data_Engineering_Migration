
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



# ⚡ Project 3: Azure Incremental Data Pipeline (Streaming‑Style)

## 📌 README.md

### Overview

High‑performance incremental ingestion pipeline for high‑volume mobility data using watermark‑based processing.

### Business Problem

* Full reloads caused delays
* High compute cost
* No near real‑time visibility

### Solution Summary

* ADF watermark‑based ingestion
* Databricks deduplication & merge logic
* Synapse analytics layer
* Power BI operational dashboards

### Business Impact

* Pipeline runtime reduced by **70%**
* Monthly compute costs reduced
* Near real‑time operational insights

---

## 🏗️ Architecture Diagram (Description)

**Flow:**
Source → ADF (Watermark) → ADLS Raw → Databricks (Merge) → ADLS Curated → Synapse → Power BI

---

## 🔧 Incremental Logic

* Maintain control table for last processed timestamp
* Filter source data using watermark
* MERGE INTO curated tables

---

## 📄 Monitoring & Governance

* Pipeline success/failure logging
* Cost‑efficient compute scaling
* Data quality checks

---

# 📚 Shared Documentation

## KPI Definitions

* Fleet Utilization = Active Time / Available Time
* Reporting Latency = Source to Dashboard SLA

## Assumptions

* Data refreshed daily or near real‑time
* ZAR as reporting currency

---

**This documentation is designed to be interview‑ready, recruiter‑friendly, and enterprise‑grade.**
