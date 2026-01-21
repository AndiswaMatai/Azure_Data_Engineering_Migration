# Azure Incremental Data Pipeline (Streaming-Style)

## Overview
Watermark-based incremental ingestion for high-volume mobility data using Azure-native components.

## Problem
Full dataset reloads delayed analytics and increased compute costs, limiting real-time insights.

## Solution
- Incremental ingestion with ADF using watermark logic
- Deduplication and transformation in Azure Databricks
- Analytics in Azure Synapse
- Real-time dashboards in Power BI

## Impact
- Pipeline execution 70% faster
- Infrastructure costs significantly reduced
- Near real-time insights enabled for mobility operations

## Tech Stack
- **Ingestion:** Azure Data Factory (watermark logic)
- **Transformation:** Azure Databricks, Python
- **Analytics:** Azure Synapse Analytics, Power BI
- **Security & Governance:** Azure AD, Key Vault

## Artifacts
- 📊 [Dashboards](./dashboards/)
- 📐 [Streaming Diagrams](./diagrams/)
- 📓 [Notebooks](./notebooks/)
- 📄 [Documentation](./documentation/)

