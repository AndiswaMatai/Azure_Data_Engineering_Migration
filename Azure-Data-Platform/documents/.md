# Documentation – Azure Data Platform

## Project Context
The organization operated fragmented on-prem SQL Server systems that slowed reporting and limited visibility into fleet and financial performance. Executives required faster, consolidated insights to improve operational efficiency.

## Architecture
- **Ingestion:** Azure Data Factory pipelines orchestrating scheduled and event-based loads
- **Storage:** Azure Data Lake Storage Gen2 for centralized, scalable data storage
- **Transformation:** Azure Databricks notebooks for cleansing, enrichment, and business logic
- **Analytics:** Curated datasets in Azure Synapse Analytics
- **Visualization:** Power BI dashboards tailored for executives
- **Security:** Azure AD for identity management, Key Vault for secrets

## Business Outcomes
- Reporting turnaround reduced from days to <2 hours
- Fleet utilization improved by 12%
- Improved trust in data quality and governance

## Lessons Learned
- Centralizing data in ADLS simplified governance
- Executive dashboards drove adoption by focusing on KPIs

