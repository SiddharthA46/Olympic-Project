Olympic Dataset Analysis Project

Overview
This project demonstrates a complete end-to-end data engineering and analytics pipeline built on the Olympic Dataset. The pipeline follows the Medallion Architecture, extracting raw data from GitHub, transforming it using Azure Databricks and Python, and storing it in Azure Data Lake. Finally, the data is visualized using Power BI to uncover actionable insights about Olympic events, athletes, and performance trends.

Architecture
The project implements the Medallion Architecture:

Bronze Layer: Stores raw data ingested from GitHub in Azure Data Lake.
Silver Layer: Applies transformations and cleaning to create structured and business-ready data.
Gold Layer: Aggregates and optimizes data for analytics and visualization.

Technologies Used
Data Extraction:
GitHub: Source of the Olympic dataset.
Azure Data Factory (ADF): Automates data ingestion into Azure Data Lake.

Data Transformation:
Azure Databricks: Performs data transformations and applies Medallion Architecture.
Python: For data wrangling, feature engineering, and custom transformations.
SQL: To structure and query data efficiently.

Data Storage:
Azure Data Lake Storage (ADLS): Stores raw, cleaned, and aggregated data.

Visualization:
Power BI: Creates interactive dashboards to analyze medal distribution, athlete performance, and trends.

Steps in the Pipeline
1. Data Ingestion
Data sourced from GitHub in CSV format.
Automated ingestion using ADF, storing the raw files in the Bronze Layer of Azure Data Lake.
2. Data Transformation
Bronze Layer: Raw data stored without modifications.
Silver Layer:
Cleaned data using Python in Azure Databricks (e.g., handling null values, renaming columns).
Combined multiple datasets (e.g., Athletes, Medals) using PySpark and SQL.
Gold Layer:
Aggregated metrics (e.g., total medals by country, athlete rankings).
Optimized queries using Delta Lake features like OPTIMIZE and ZORDER.
3. Data Visualization
Power BI Dashboards:
Medal Distribution: Total medals by country and type (gold, silver, bronze).
Athlete Insights: Trends in participation and performance over the years.
Event Analysis: Key trends in popular Olympic events.
