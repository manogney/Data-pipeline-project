#  Enterprise Data Integration Platform

A scalable Data Engineering project that implements an end-to-end ETL pipeline using the Medallion Architecture (Bronze, Silver, Gold). The pipeline ingests raw transactional data, performs data cleansing and transformations, and loads curated fact and dimension tables to support analytical reporting.

## Project Overview

This project demonstrates a modern data engineering workflow by processing sales and customer data through multiple data layers. It supports both historical and incremental data loading while maintaining clean, analytics-ready datasets.

The pipeline follows the Medallion Architecture:

- **Bronze Layer** – Stores raw source data.
- **Silver Layer** – Cleanses, validates, and transforms data.
- **Gold Layer** – Creates business-ready fact and dimension tables for analytics.
## Architecture



