# 🚀 AdventureWorks DWH Pipeline

A PySpark-based ETL pipeline that transforms the transactional `AdventureWorks` OLTP database into a dimensional Data Warehouse (DWH) ready for analysis and visualization in Power BI.

---

## 📦 Project Overview

This project simulates a real-world data engineering workflow by:
- Extracting data from the **AdventureWorks** SQL Server database
- Transforming normalized OLTP data into a **star-schema DWH model**
- Loading fact and dimension tables into a **data lake** in **Parquet/Delta format**
- Preparing datasets for **Power BI** dashboards

> This project is for **educational purposes** and is designed to demonstrate ETL design, PySpark transformation, and warehouse modeling using open Microsoft data.

---

## 🧱 Architecture

```text
AdventureWorks (OLTP SQL Server)
        |
     [PySpark]
 ┌─────┼────────────┐
 │  Extract         │
 │  Transform       │ --> Star Schema (Fact + Dimensions)
 │  Load            │
 └─────┼────────────┘
        |
   Data Lake (Parquet / Delta / CSV)
        |
   Power BI (Visualization Layer)
