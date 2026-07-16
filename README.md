#  Enterprise Data Integration Platform

A scalable Data Engineering project that implements an end-to-end ETL pipeline using the Medallion Architecture (Bronze, Silver, Gold). The pipeline ingests raw transactional data, performs data cleansing and transformations, and loads curated fact and dimension tables to support analytical reporting.

## Project Overview

This project demonstrates a modern data engineering workflow by processing sales and customer data through multiple data layers. It supports both historical and incremental data loading while maintaining clean, analytics-ready datasets.

The pipeline follows the Medallion Architecture:

- **Bronze Layer** – Stores raw source data.
- **Silver Layer** – Cleanses, validates, and transforms data.
- **Gold Layer** – Creates business-ready fact and dimension tables for analytics.
## Architecture

<img width="20005" height="11129" alt="project_architecture" src="https://github.com/user-attachments/assets/7569241a-b520-45b3-b457-25a09a114fbe" />

## Dataset

### Source Files

- Customers
- Products
- Gross Price
- Daily Orders

### Gold Layer Tables

- `dim_customers`
- `dim_products`
- `dim_gross_price`
- `fact_orders`

- ## Features

- Historical Data Loading
- Incremental Data Loading
- Data Cleaning and Validation
- Fact and Dimension Modeling
- Medallion Architecture
- SQL-based ETL Transformations
- Business-ready Gold Layer
- Scalable Data Pipeline Design
## Technologies Used

- Databricks
- Apache Spark
- PySpark
- SQL
- Delta Lake
- Unity Catalog
- CSV Files
- Medallion Architecture

## ETL Workflow

### Bronze Layer

- Load raw CSV files
- Preserve original data
- Handle schema inference

### Silver Layer

- Remove duplicate records
- Handle missing values
- Convert data types
- Apply business transformations
- Standardize data

### Gold Layer

Create analytical tables:

- Customer Dimension
- Product Dimension
- Gross Price Dimension
- Sales Fact Table

## Incremental Loading

The pipeline supports incremental data processing by loading only newly arrived records while preserving historical data.

### Workflow

1. Detect newly arrived source files.
2. Process the data through the Bronze and Silver layers.
3. Generate incremental Fact and Dimension tables in the Child Gold layer.
4. Load the incremental records into a **staging table**.
5. Validate and transform the staged data.
6. Merge the staged records into the Parent Gold tables using SQL, ensuring only new or updated records are applied.
7. Maintain a unified enterprise-ready Gold layer for downstream analytics and reporting.

# OUTPUT


