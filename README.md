# Azure End-to-End Data Engineering Project
## Project Overview

This project demonstrates the implementation of an end-to-end data engineering pipeline using **Azure Data Factory (ADF), Azure Data Lake Storage Gen2 (ADLS Gen2), and Azure Databricks**. The solution ingests data from multiple sources, including APIs, CSV files, Parquet files, and real-time event streams, and processes it using the Medallion Architecture.

Azure Data Factory handles data ingestion and movement into ADLS Gen2, while Databricks processes and transforms the data across the Bronze, Silver, and Gold layers. Databricks Spark Declarative Pipelines are used to build streaming tables and temporary views, implement Slowly Changing Dimension (SCD) Type 2 logic, and maintain historical changes in the Silver and Gold layers.

Databricks Workflows orchestrate and schedule pipeline tasks based on dependencies, enabling automated execution of the end-to-end process. All processed data remains in ADLS Gen2 external storage, where curated datasets are made available for downstream consumption by business intelligence tools such as Tableau and Power BI, as well as machine learning and advanced analytics teams.

## Architecture & Workflow

1. **Data Ingestion:** Use Azure Data Factory to ingest data from APIs, CSV files, Parquet files, and real-time data sources.
2. **Data Landing:** Store ingested data in Azure Data Lake Storage Gen2.
3. **Data Processing:** Use Azure Databricks and PySpark to clean, transform, validate, and process data through the Bronze, Silver, and Gold layers.
4. **Declarative Pipelines:** Create streaming tables and temporary views, apply data quality rules, and implement SCD Type 2 to maintain historical records.
5. **Orchestration:** Use Databricks Workflows to schedule jobs, manage task dependencies, and automate pipeline execution.
6. **Data Consumption:** Store curated datasets in ADLS Gen2 for consumption by Tableau, Power BI, and machine learning teams.


## Medallion Architecture

- **Bronze Layer:** Stores raw ingested data.
- **Silver Layer:** Stores cleaned, validated, and transformed data, with SCD Type 2 processing where required.
- **Gold Layer:** Contains business-ready, curated datasets and historical dimension records for analytics and reporting.

## Technologies Used

- **Cloud Platform:** Microsoft Azure
- **Data Ingestion:** Azure Data Factory
- **Data Storage:** Azure Data Lake Storage Gen2
- **Data Processing:** Azure Databricks, PySpark, Spark SQL
- **Pipeline Development:** Spark Declarative Pipelines
- **Data Architecture:** Medallion Architecture (Bronze, Silver, Gold)
- **Data Modeling:** Slowly Changing Dimension (SCD) Type 2
- **Orchestration:** Databricks Workflows
- **Data Consumption:** Tableau, Power BI, Machine Learning


## Key Highlights

- Built an end-to-end data pipeline integrating multiple data sources.
- Implemented a scalable lakehouse architecture using ADLS Gen2 and Databricks.
- Developed batch and streaming data processing workflows.
- Implemented SCD Type 2 for historical data tracking.
- Automated pipeline execution using scheduled workflows and task dependencies.
- Centralized processed data in external cloud storage for downstream analytics and machine learning.

## Data Flow

**Multiple Sources → Azure Data Factory → ADLS Gen2 → Azure Databricks → Bronze / Silver / Gold → Databricks Workflows → Curated Data in ADLS Gen2 → Tableau / Power BI / Machine Learning**

