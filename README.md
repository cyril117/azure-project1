Tokyo Olympics Azure Data Engineering Project
Project Overview

This project demonstrates an end-to-end Azure Data Engineering pipeline using Tokyo Olympics datasets. The pipeline ingests raw CSV files, stores them in Azure Data Lake Storage Gen2, performs transformations using Azure Databricks and PySpark, and visualizes insights in Power BI.

Architecture
GitHub Dataset
      ↓
Azure Data Factory
      ↓
Azure Data Lake Storage Gen2 (Raw Layer)
      ↓
Azure Databricks (PySpark Transformations)
      ↓
Transformed Data (Processed Layer)
      ↓
Power BI Dashboard
Technologies Used
Azure Data Factory
Azure Data Lake Storage Gen2
Azure Databricks
PySpark
Power BI
GitHub
Python
Datasets Used

The project uses Tokyo Olympics datasets such as:

Athletes.csv
Coaches.csv
EntriesGender.csv
Medals.csv
Teams.csv
Project Workflow
1. Data Ingestion
Raw CSV datasets were collected from GitHub.
Azure Data Factory was used to ingest data into ADLS Gen2.
2. Data Storage
Data stored in Azure Data Lake Storage Gen2.
Folder structure created using virtual directories.

Example:

raw-data/
transformed-data/
3. Data Transformation

PySpark transformations were performed in Azure Databricks.

Transformations included:

Removing null values
Removing duplicates
Filtering records
Aggregations
Grouping and sorting
Creating new columns

Example:

df_clean = df.dropna()

country_df = df.groupBy("Country") \
               .count()
4. Data Visualization

Power BI dashboards were created to analyze:

Male vs Female athlete participation
Medal distribution
Country-wise performance
Discipline analysis
Coach analysis
Sample Power BI Dashboards
Gender Participation Analysis
Top Countries by Medals
Discipline-wise Athlete Count
Country Performance Dashboard
