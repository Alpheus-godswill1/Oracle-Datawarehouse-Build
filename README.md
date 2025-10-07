# 💧 Water Quality Data Warehouse Project

Design and implement a fully functional **Data Warehouse** solution for environmental water quality monitoring using **Oracle Database**, **SQL**, **PL/SQL**, and **Python**.

This project was developed as part of a data warehousing coursework, focused on solving real-world analytical and data integration challenges using structured design principles, ETL workflows, and advanced SQL operations.

---

## 📘 Project Overview

Traditional water quality monitoring relies on manual sampling and lab-based testing, which is time-consuming and expensive. This project aims to build a **data warehouse** that provides automated, accurate, and real-time analytical insights into water quality data obtained from the **Department for Environment, Food & Rural Affairs (DEFRA)**.

The data warehouse integrates, cleanses, and organizes environmental data from various sampling points across England — rivers, lakes, coastal waters, and more — to enable decision-makers to analyze pollutant trends, sensor activity, and overall water quality over time.

---

## 🧱 Key Features

- **Star Schema Design**
  Developed a **data mart** using a star schema architecture, including fact and dimension tables (Time, Sensor, Location, Measurement Type).

- **ETL Pipeline Implementation**

  - Extracted raw data from a **Microsoft Access** database.
  - Transformed and cleansed data in a **staging area** before loading it into Oracle.
  - Automated data loading using **PL/SQL cursors** and reusable scripts.

- **Data Cleansing and Validation**

  - Identified and corrected missing keys, duplicates, and invalid entries.
  - Removed redundant columns and imputed missing values where necessary.
  - Documented all cleansing steps for reproducibility.

- **Analytical Query Support**
  Developed SQL scripts to answer critical analytical questions, including:

  - List of water sensors by type per month
  - Number of sensor measurements by week and by location
  - Average **pH** levels and **nitrate** measurements per year
  - Yearly pollutant trend analysis across multiple regions

- **Oracle–Python Integration**

  - Established a connection between **Python** and **Oracle Database** for automated data retrieval.
  - Executed analytical queries and generated statistical summaries directly from Python.
  - Prepared datasets for visualization and reporting.

- **Materialized Views and Partitioning (Bonus)**

  - Created **materialized views** for two-year average trend analysis.
  - Implemented **table partitioning** by year to optimize query performance.
  - Extended the **Time Dimension** to support long-term analytical queries.

---

## 🧩 Architecture

**Core Components:**

- **Data Source:** DEFRA Water Quality Dataset (2000–2016)
- **Staging Area:** Temporary schema for data cleansing and transformation
- **Data Warehouse Schema:** Star schema with fact and dimension tables
- **ETL Process:** Extract → Transform → Load using SQL and PL/SQL
- **Integration Layer:** Python scripts for analysis and reporting

---

## 🧠 Data Warehouse Design

**Star Schema Includes:**

- **Fact Table:** `Fact_WaterQuality` — contains measurement data linked to dimensions
- **Dimensions:**

  - `Dim_Sensor` — details of sensor types and categories
  - `Dim_Location` — sampling points and geographic information
  - `Dim_Time` — dates, months, quarters, and years
  - `Dim_Parameter` — pollutant or water quality parameter information

Each dimension is linked by surrogate keys, ensuring efficient analytical queries and minimal redundancy.

---

## ⚙️ Technologies Used

- **Oracle Database** – Core data warehouse engine
- **Microsoft Access** – Original source dataset
- **SQL / PL/SQL** – ETL scripting, queries, and data transformation
- **Python (cx_Oracle)** – Integration, data retrieval, and analysis
- **Data Modeling Tools** – ER/Studio, SQL Developer Data Modeler

---

## 🚀 Implementation Highlights

- Created and populated **fact and dimension tables** using cursor-based PL/SQL procedures.
- Automated **ETL processes** and stored scripts for reuse and scalability.
- Implemented **error handling and logging** for ETL failures.
- Used **SQL\*Loader** to import flat files into Oracle tables efficiently.
- Designed a **BUS Matrix** to map business processes to corresponding dimensions and measures.

---

## 📊 Example Analytical Outputs

- **Sensor Activity Report:** Number of measurements per sensor type, grouped by month
- **Location Trend Analysis:** Average pollutant readings per geographic region
- **Nitrate and pH Analysis:** Yearly average concentration by location
- **Time-based Insights:** Materialized view showing pollutant averages every two years

---

## 🧩 Python Integration

Python scripts were developed to:

- Connect to Oracle Database using `cx_Oracle`
- Execute SQL queries from the data warehouse
- Perform lightweight preprocessing and data summarization
- Generate visual summaries (optional extension)

Example functions include:

- `connect_to_oracle()` – Establishes secure DB connection
- `execute_query()` – Retrieves and displays analytical results
- `fetch_summary()` – Aggregates key statistics for reporting

---

## 🧪 Bonus Features Implemented

- Extended **Time Dimension** to support daily, weekly, monthly, and yearly aggregation.
- Created a **Materialized View** for average pollutant concentration every two years.
- Automated **Data Cleansing Tool** using PL/SQL functions.
- Partitioned **Fact Table by Year** to enhance performance and manage large datasets.

---

## 🧾 Deliverables

- Star Schema Design Diagram & BUS Matrix
- ETL Scripts (SQL / PL/SQL)
- Data Cleansing Scripts & Documentation
- Analytical SQL Queries
- Python–Oracle Connection Scripts
- Report and Screenshots of GUI Queries

---

## 🧰 Skills Demonstrated

- Data Warehouse Architecture & Design
- ETL Development (SQL, PL/SQL, Python)
- Data Cleansing and Quality Assurance
- Dimensional Modeling & Star Schema Implementation
- Performance Optimization (Partitioning, Materialized Views)
- Database Connectivity and Data Visualization

---

## 📎 References

- DEFRA Water Quality Archive: [Environment Data Service](https://environment.data.gov.uk/)
- Oracle Database Documentation
- cx_Oracle Python Library Documentation

---

### 📚 Summary

This project demonstrates the **end-to-end lifecycle** of a data warehousing solution — from raw data extraction and cleansing to analytics and reporting — applying both **database engineering** and **data analysis** concepts. It bridges traditional data management with modern analytical workflows, showcasing technical proficiency in **Oracle, SQL, PL/SQL, and Python**.
