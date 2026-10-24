# End-to-End ELT Data Pipeline using Snowflake & Snowpark (Python)

[![Snowflake](https://img.shields.io/badge/Snowflake-00A1E9?style=for-the-badge&logo=snowflake&logoColor=white)](https://www.snowflake.com/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Snowpark](https://img.shields.io/badge/Snowpark-Data%20Engineering-29B5E8?style=for-the-badge)](https://docs.snowflake.com/en/developer-guide/snowpark/python/index)

This repository demonstrates a modern **Extract, Load, Transform (ELT)** data engineering pipeline built inside **Snowflake** using **Snowpark for Python**. The project covers the end-to-end process of setting up raw data tables, performing data transformations using Python DataFrames natively inside Snowflake, loading data into a dimensional model, and running automated data validation checks.

---

## Pipeline Steps
1. **Environment Setup:** Programmatically provision Snowflake databases, schemas (`RAW`, `ANALYTICS`), and compute resources.
2. **Data Ingestion:** Simulate raw transactional ingestion into staging tables (`DE_SAMPLE_DB.RAW.RAW_ORDERS`).
3. **Transformation:** Utilize Snowpark Python DataFrames to clean strings, parse dates, and filter out cancelled transactions directly in Snowflake's warehouse engine.
4. **Dimensional Modeling:** Write transformed data into an analytical schema (`DE_SAMPLE_DB.ANALYTICS`) formatted into target tables (`dim_customers` and `fact_orders`).
5. **Data Quality & Metrics:** Perform integrity checks and calculate summary statistics to ensure data readiness.

---

## 🛠️ Tech Stack & Prerequisites

* **Data Warehouse:** Snowflake
* **Language:** Python 3.8+
* **Framework:** Snowflake Snowpark API for Python
* **Notebook Platform:** Snowflake Notebooks / Jupyter Notebook

### Prerequisites:
- A Snowflake account (or trial account) with `SYSADMIN`, `ACCOUNTADMIN`, or equivalent privileges.
- Python 3.8+ installed (if running locally outside Snowflake Notebooks).
- `snowflake-snowpark-python` library installed.

---

## 🚀 Quickstart Guide

### Option A: Running directly in Snowflake Worksheets / Notebooks (Recommended)
1. Log into your **Snowflake Snowsight UI**.
2. Navigate to **Projects** > **Notebooks**.
3. Create a new notebook, select **Python (Snowpark)** as the environment.
4. Import `snowflake_snowpark_elt_pipeline.ipynb` and run the cells sequentially.

### Option B: Running locally via Jupyter
1. Clone the repository:
   ```bash
   git clone [https://github.com/](https://github.com/)<your-username>/snowflake-snowpark-elt-pipeline.git
   cd snowflake-snowpark-elt-pipeline
