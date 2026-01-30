🚴 Building the Bike Data Lakehouse

Databricks End-to-End Data Engineering & Machine Learning Project

📌 Overview

This project demonstrates an end-to-end Lakehouse implementation on Databricks, transforming raw bike sales data into analytics-ready datasets and machine learning–driven sales predictions.

The solution follows industry best practices in data engineering, analytics, and ML system design using a Bronze → Silver → Gold architecture.

🎯 Problem Statement

Retail organizations often face challenges such as:

Raw data scattered across files and systems

Poor data quality and inconsistent schemas

Limited integration between analytics and machine learning

No clear end-to-end data → AI workflow

This project addresses these challenges by building a scalable, governed, and ML-ready data platform.

🏗️ Architecture Overview

The solution is built using the Databricks Lakehouse architecture:

Bronze (Raw Ingestion)
   → Silver (Cleaned & Standardized)
       → Gold (Business & ML-Ready)


Each layer has a clearly defined responsibility, ensuring traceability, data quality, and scalability.

📂 Data Layers
🥉 Bronze Layer

Raw CSV files ingested into Delta tables

Minimal transformation to preserve source fidelity

Source-system–prefixed table naming for lineage

🥈 Silver Layer

Data cleaning and standardization

Duplicate handling and schema enforcement

String and date validation

Business-ready structured datasets

🥇 Gold Layer

Fact and dimension modeling

Analytics-ready tables

Direct input for machine learning

ML predictions written back to Gold tables

📊 Analytics

The Gold layer supports:

Product-level and category-level sales analysis

Revenue and quantity trend analysis

Insights that directly inform feature engineering for ML

Analytics are designed not just for reporting, but to drive better ML decisions.

🤖 Machine Learning

Use case: Sales prediction (regression)

Features: Quantity, price, product cost, category, subcategory

Model: Linear Regression (interpretable baseline)

Evaluation: RMSE and R²

Tracking: MLflow for experiments, metrics, and artifacts

Predictions are stored in a Gold Delta table, completing the Database ↔ AI workflow.

🧪 Tools & Technologies

Databricks

Apache Spark (PySpark, Spark SQL)

Delta Lake

MLflow

Python
