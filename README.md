# Netflix-Azure-Data-Engineering-Project
Introduction:
In this project, I built a highly scalable data pipeline for processing and analyzing Netflix dataset using Azure Data Engineering Stack. The goal was to build an end-to-end ETL solution that efficiently ingests, transforms, and visualizes data in Databricks, Delta Live Tables (DLT), Azure Synapse, and Power BI.

🔧 Tech Stack & Tools Used:
✅ Databricks: Used for data processing, transformation, and orchestration
✅ Delta Live Tables (DLT): Implemented incremental data processing with autoloader
✅ Azure Data Factory (ADF): For data ingestion & workflow automation
✅ Azure Data Lake Gen2: Storage layer for Bronze, Silver, and Gold tables
✅ Azure Synapse Analytics: Warehouse for querying structured data
✅ Power BI: For interactive dashboards and visualizations
✅ GitHub: Version control & collaboration
✅ Azure Key Vault: Secure storage of credentials
✅ dbutils: Databricks Utilities for handling widgets, secrets, and storage

📂 Data Pipeline Architecture:
📌 Ingestion Layer: Data is loaded incrementally using Databricks Autoloader from Azure Data Lake.
📌 Bronze Layer (Raw Data Store): Stores raw ingested data in Delta format.
📌 Silver Layer (Transformations & Cleansing): Applied validations, deduplication, and aggregations.
📌 Gold Layer (Star Schema): Data is structured for analytics & reporting.
📌 Orchestration: Used Databricks Workflows and Azure Data Factory for scheduling jobs.
📌 Visualization: Power BI connected to Azure Synapse for interactive reporting.

🔹 ⚡ Key Implementations & Optimization Techniques
🔹 Incremental Loading:
✅ Used Databricks Autoloader for continuous ingestion with checkpointing.
✅ Ensured idempotency to avoid duplicate data loads.

🔹 Delta Live Tables for Streaming & Batch Processing
✅ Implemented Change Data Capture (CDC) using Delta format.
✅ Used @dlt.table and @dlt.expect_all_or_drop() to enforce data quality checks.

🔹 Orchestration with Conditional Execution
✅ Implemented ForEach & If-Else Conditions to execute specific jobs based on day of execution.
✅ Leveraged dbutils.jobs.taskValues.set() for cross-task communication.

🔹 Optimizations using Databricks SQL
✅ Used OPTIMIZE & ZORDER BY to speed up queries & partition pruning.
✅ Data Skipping to reduce scan times on large datasets.

🔹 Security & Access Control
✅ Configured Azure Key Vault to store secrets & credentials securely.
✅ Used dbutils.secrets.get() to retrieve authentication tokens securely.

🔹 Outcome & Impact
🔥 End-to-end ETL Pipeline successfully processes Netflix dataset with high efficiency & scalability.
🔥 Automated workflow execution with Databricks Workflows & ADF reduces manual effort.
🔥 Optimized queries & data warehouse design lead to faster analytics in Power BI.
🔥 Fully secure environment with Azure Key Vault integration.
