# End-to-End ELT Data Pipeline using Snowflake & Snowpark (Python)

[![Snowflake](https://img.shields.io/badge/Snowflake-00A1E9?style=for-the-badge&logo=snowflake&logoColor=white)](https://www.snowflake.com/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Snowpark](https://img.shields.io/badge/Snowpark-Data%20Engineering-29B5E8?style=for-the-badge)](https://docs.snowflake.com/en/developer-guide/snowpark/python/index)

This repository demonstrates a modern **Extract, Load, Transform (ELT)** data engineering pipeline built inside **Snowflake** using **Snowpark for Python**. The project covers the end-to-end process of setting up raw data tables, performing data transformations using Python DataFrames natively inside Snowflake, loading data into a dimensional model, and running automated data validation checks.

---

## 🏗️ Architecture & Data Flow

+------------------+      +---------------------+      +------------------------+
|  Raw Data Layer  | ---> | Transformation Layer | ---> |  Analytics Data Layer  |
|  (JSON / CSV)    |      | (Snowpark DataFrames)|      | (Dim & Fact Models)    |
+------------------+      +---------------------+      +------------------------+
|
v
+----------------------+
| Data Quality &       |
| Validation Checks    |
+----------------------+
