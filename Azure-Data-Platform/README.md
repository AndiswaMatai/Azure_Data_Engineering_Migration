# Azure Data Engineering Migration Portfolio – Project Documentation

This document contains **README content, architecture descriptions, pipeline logic, scripts outline, and governance documentation** for all three Azure Data Engineering projects. Each section can be copied directly into its respective project folder.

---

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

# 📊 Project 2: SQL Server → Power BI Modernization

## 📌 README.md

### Overview

Modernization of legacy SQL Server reporting into a scalable, cloud‑native Azure analytics platform enabling self‑service BI.

### Business Problem

* Manual Excel extracts
* Long refresh cycles
* Limited scalability and access control

### Solution Summary

* Automated ingestion via Azure Data Factory
* Transformations using Databricks
* Synapse analytics layer for Power BI
* Certified datasets for enterprise use

### Business Impact

* Reporting latency reduced to **~12 hours**
* Power BI adoption scaled to **550+ users**
* Department‑level drilldowns enabled
* Financial KPIs reported in **ZAR**

---

## 🏗️ Architecture Diagram (Description)

**Flow:**
SQL Server → ADF → ADLS Gen2 → Databricks → Synapse → Power BI Service

**Key Concepts:**

* Star schema modeling
* Certified datasets
* Incremental refresh

---

## 🔧 Pipeline & Script Logic

### Databricks

* Dimension & fact table construction
* Surrogate keys
* Slowly Changing Dimensions (Type 2)

### Power BI

* Semantic model with measures
* Row Level Security (RLS)

---

## 📄 Governance

* Dataset certification
* Workspace separation (Dev / Test / Prod)
* Refresh monitoring

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
