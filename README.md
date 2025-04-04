# CLOUD-FLIX(netflix-azure)
**Cloud-Flix** is a comprehensive project focused on Azure Data Engineering, Big Data Processing, and ETL Development, covering a range of real-world implementations. This project involves building an end-to-end data pipeline, ensuring efficient data ingestion, transformation, and orchestration using **Azure Data Factory (ADF)** and **Databricks**. Leveraging **Azure Data Lake Storage Gen2 (ADLS Gen2)** ensures a structured, scalable, and secure data architecture. The multi-layered pipeline (Raw → Bronze → Silver → Gold) handles data ingestion, transformation, and processing efficiently.

## Key Project Highlights

- **Scalable Azure Data Architecture (ADLS Gen2)**: Designed and optimized data pipeline and data processing framework.
- **Azure Data Factory (ADF)**: Developed ETL pipelines for seamless data ingestion.
- **Databricks & Unity Catalog**: Ensured secure data governance and access control.
- **Incremental Data Loading with Autoloader**: Automated smooth and real-time data updates.
- **Spark Streaming**: Processed streaming data efficiently for real-time insights.
- **PySpark & Data Transformation**: Leveraged PySpark for data cleansing, transformation, and wrangling.
- **Delta Live Tables**: Built a robust and scalable data pipeline with Delta Lake.
- **Databricks Workflows**: Automated end-to-end data orchestration.
- **Big Data Analytics with Apache Spark**: Performed large-scale data processing and analytics.
- **End-to-End Implementation**: Successfully integrated all components into a streamlined workflow.

## Key Learnings & Takeaways

- **Leveraging ADLS Gen2 for Efficient Storage**: Utilized Azure Data Lake Storage Gen2 with hierarchical namespace enabled, ensuring optimized performance, security, and cost-effective storage for structured data lakes.
- **ADF Activities & Dynamic Workflows**: Created Linked Services, Copy Activity, ForEach loops, and dynamic parameterization, enabling automated data ingestion into Bronze layer (container) of ADLS Gen2 scalable storage from GitHub REST API.
- **Access Connector, Unity Catalog, Metastore, and Storage Locations**: Set up metastore and used access connector (linked with storage account IAM) and defined Metastore, attached workspace, enforced fine-grained access control, and managed structured data efficiently across the Databricks workspace.
- **Real-Time Streaming Data Processing with PySpark**: Implemented Databricks Autoloader to efficiently ingest real-time streaming data into the Bronze layer, ensuring fault-tolerant and scalable processing.
- **Transformations with PySpark**: Used PySpark DataFrames to clean, filter, and perform aggregations, ensuring optimized transformations and efficient incremental data loads in the Silver Layer.
- **Workflows in Databricks**: Designed Databricks Workflows using task dependencies, taskValues, and dynamic Lookup Arrays, ensuring seamless transformation from Bronze to Silver layer based on metadata-driven logic.
- **Delta Live Tables (DLT)**: Leveraged DLT Pipelines for real-time data validation, schema enforcement, and automated data quality checks, ensuring accurate and consistent Gold layer processing.

## Data Pipeline Architecture

### Bronze Layer – Raw Data Ingestion
- **Azure Data Factory (ADF)** is used to ingest data from GitHub (REST API) into **Azure Data Lake Storage Gen2 (ADLS Gen2)**.
- Developed parameterized pipelines with file validation checks to ensure data integrity.
- The ingestion process is scheduled weekly to handle periodic updates.

### Silver Layer – Data Transformation
- **Azure Databricks** and **PySpark** are used for data cleansing and transformation.
- Implemented **Databricks Auto-loader** for incremental batch ingestion, ensuring fact table processing occurs every Monday.
- The **Access Connector** is used to securely connect **Unity Catalog** with ADLS Gen2, enabling metadata management and governance.
- The cleaned data is stored in **Parquet** format in the Silver Layer for further processing.

### Gold Layer – Optimized Data for Analytics
- Utilized **Delta Live Tables (DLT)** to process batch-based dimensional data tables for analytics.
- Enabled schema evolution to handle structural changes in incoming data.
- Optimized data storage for faster querying and reporting.

## Technologies Used
- **Azure Data Lake Storage Gen2 (ADLS Gen2)**
- **Azure Data Factory (ADF)** – Parameterized Pipelines
- **Azure Databricks & PySpark**
- **Databricks Auto-loader** – Incremental Ingestion
- **Delta Live Tables (DLT)**
- **Azure Access Connector** – Unity Catalog Integration

