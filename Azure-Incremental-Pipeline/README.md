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
