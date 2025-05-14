# 🚦 Real-Time Traffic & Roads Data Pipeline

This project simulates a real-time data engineering pipeline using traffic and road datasets. Built on **Azure Databricks** and **Azure Data Lake Storage Gen2**, it leverages the **Medallion Architecture** to ingest, transform, and serve data through Bronze, Silver, and Gold layers. The solution also integrates **Spark Structured Streaming**, **Delta Lake**, **Unity Catalog**, and **CI/CD** best practices for production-grade data engineering.

---

## 🧭 Project Objectives

- Simulate a real-time ETL pipeline using traffic and road data.
- Ingest and transform data using **Structured Streaming** with **Autoloader**.
- Apply Medallion Architecture: Bronze → Silver → Gold layers.
- Govern data access and manage metadata using **Unity Catalog**.
- Implement **CI/CD** pipelines for deployment and automation.
- Enable observability and fault-tolerance with **Delta Live Tables**.

---

## 🧰 Tech Stack

| Category               | Tools/Technologies                             |
|------------------------|------------------------------------------------|
| Cloud Platform         | Azure Data Lake Gen2, Azure DevOps             |
| Processing Engine      | Apache Spark (Structured Streaming)            |
| Notebook Environment   | Azure Databricks (with Unity Catalog)          |
| Storage Format         | Delta Lake                                     |
| Pipeline Orchestration | Delta Live Tables, Azure DevOps Pipelines      |
| Governance             | Unity Catalog                                  |

---

## 🏗️ Architecture Overview
Landing Zone (ADLS Gen2)
↓ (Autoloader + Structured Streaming)
Bronze Layer (Raw Ingestion)
↓ (Transformations - Filtering, Parsing)
Silver Layer (Cleaned, Modeled Data)
↓ (Minimal Aggregation)
Gold Layer (Reporting & Consumption)



---

## 🧪 Features

- ✅ Incremental & real-time ingestion with **Spark Autoloader**
- ✅ **Delta Lake** for ACID compliance and time travel
- ✅ **Unity Catalog** for centralized governance
- ✅ **CI/CD** pipeline to deploy notebooks, workflows & access policies
- ✅ Real-time transformation using **Structured Streaming**
- ✅ **Delta Live Tables** for declarative data pipeline management

---

## 📁 Project Structure (Example)
```
Real-Time-Traffic-Pipeline/
├── notebooks/
│ ├── 01_landing_to_bronze_stream.py
│ ├── 02_bronze_to_silver.py
│ ├── 03_silver_to_gold.py
│ └── utils/
├── pipelines/
│ └── delta_live_config.json
├── ci_cd/
│ └── azure_pipeline.yml
├── unity_catalog/
│ ├── schema_definitions/
│ └── access_controls/
├── data_samples/
│ ├── traffic_data.csv
│ └── roads_data.csv
└── README.md
```

---

## 🚀 How to Run the Project

1. **Upload datasets** to ADLS Gen2 container (`landing-zone`).
2. Run `01_landing_to_bronze_stream.py` in Databricks to ingest data using Autoloader.
3. Execute transformation notebooks in sequence.
4. Configure Unity Catalog with `schema_definitions` and ACLs.
5. Trigger Azure DevOps pipeline for CI/CD deployment.
6. Monitor pipeline execution via Delta Live Tables UI.

---

## 📊 Expected Output

- Real-time dashboards powered by clean, structured data.
- Auditable data governance with Unity Catalog.
- Automated deployment and version control of all data assets.

---

## 🧠 Key Concepts Demonstrated

- Medallion Architecture (Bronze, Silver, Gold)
- Structured Streaming and Incremental Loads
- Unity Catalog (Object Model & Access Control)
- Delta Live Tables and CI/CD for production pipelines

---

## 🧠 Key Concepts Demonstrated

- Medallion Architecture (Bronze, Silver, Gold)
- Structured Streaming and Incremental Loads
- Unity Catalog (Object Model & Access Control)
- Delta Live Tables and CI/CD for production pipelines

---

## 📌 Notes

- This project simulates a real-time production scenario using historical data.
- No sensitive data is included—datasets are synthetic or anonymized.

---



