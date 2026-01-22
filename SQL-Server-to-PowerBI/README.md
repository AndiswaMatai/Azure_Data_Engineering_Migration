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

