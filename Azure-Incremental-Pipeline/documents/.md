# Documentation – Azure Incremental Data Pipeline (Streaming-Style)

## Project Context
High-volume mobility data required frequent refreshes. Full dataset reloads delayed analytics and increased compute costs, limiting near real-time insights.

## Architecture
- **Ingestion:** Azure Data Factory with watermark-based incremental logic
- **Transformation:** Deduplication and enrichment in Azure Databricks
- **Analytics:** Synapse datasets supporting near real-time queries
- **Visualization:** Power BI dashboards showing pipeline execution metrics and mobility KPIs
- **Security:** Azure AD for access control, Key Vault for secure secrets

## Business Outcomes
- Pipeline execution 70% faster
- Infrastructure costs reduced significantly
- Near real-time insights enabled for mobility operations

## Lessons Learned
- Incremental ingestion reduced compute overhead
- Deduplication logic ensured data accuracy

