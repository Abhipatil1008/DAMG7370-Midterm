# LA Crime Analysis (Databricks + Delta Lake + Power BI)

End-to-end analytics project on **Los Angeles crime incidents** using a **Medallion (Bronze/Silver/Gold) pipeline** in Databricks, a **star schema** for reporting, and interactive **Power BI dashboards** for trends, hotspots, and crime patterns.

---

## Project Goals
- Build a reliable data pipeline for LA crime data (raw → cleaned → analytics-ready).
- Design a dimensional model (star schema) to support fast BI reporting.
- Answer key questions:
  - How does crime change over time (year/month/quarter)?
  - What are the most common crime types and where do they occur?
  - How do day/time/week factors affect crime frequency?
  - Which areas show higher crime density (hotspots)?

---

## Tech Stack
- **Databricks** (Spark, Delta Lake, Delta Live Tables optional)
- **Python (PySpark)** for ingestion + transformation
- **SQL** for modeling + validation
- **Power BI** (DirectQuery/Import) for dashboards
- **GitHub** for version control + documentation

---

## Dataset
- **Source:** LA Open Data (Los Angeles Police Department crime incidents)
- **Granularity:** Incident-level records (date/time, location, crime code/desc, area, weapon, victim info, status, etc.)
- **Note:** Dataset may include missing/invalid coordinates, inconsistent text fields, and schema drift over time.

----------------------------------------------------------------------------------------------------------------------------------------

# 🎬 IMDb Data Warehouse & Analytics Project

## 📌 Project Overview
This project implements an **end-to-end analytical data warehouse for IMDb data**, designed to support complex analytical queries related to movies, TV series, cast & crew, genres, languages, regions, and ratings.

The solution follows a **Medallion Architecture (Bronze → Silver → Gold)** using **Databricks**, and exposes analytics through **Power BI** using a **star-schema–based dimensional model**.

The goal is to transform raw IMDb datasets into **business-ready, analytics-optimized tables** that enable rich reporting and insights.

---

## 🏗️ Architecture Overview

IMDb Raw Datasets  
→ Bronze Layer (Raw Ingestion)  
→ Silver Layer (Cleaned & Standardized)  
→ Gold Layer (Dimensional Model)  
→ Power BI Analytics (DirectQuery)

---

## 🧱 Data Layers

### 🔹 Bronze Layer (Raw)
- Raw IMDb datasets ingested with minimal transformation
- Schema preserved
- Stored as Delta tables

### 🔹 Silver Layer (Cleansed & Enriched)
- Null handling (`\N` → NULL)
- Data type casting & validation
- Exploding multi-valued fields
- Standardized language & region codes
- Data quality rules

### 🔹 Gold Layer (Analytics-Ready Star Schema)

#### ⭐ Dimensions
- dim_title
- dim_person
- dim_genre
- dim_language
- dim_region
- dim_profession

#### 🔗 Bridge Tables
- bridge_title_genre
- bridge_title_person
- bridge_title_language
- bridge_title_region
- bridge_person_profession

#### 📊 Fact Table
- fact_title_ratings

---

## 📈 Business Questions Answered
- Professions per person (primary & secondary)
- People with multiple professions
- Genres for a given title
- Movies released by year
- Runtime analysis by year
- Adult vs non-adult titles
- Languages & regions per title
- Popular directors & writers
- Episodes per season
- Cast & crew roles per title
- Top-rated movies by year & genre

---

## 📊 Power BI Reporting
- Connected via DirectQuery
- Star schema relationships
- Interactive slicers & charts
- Ranking and aggregation visuals

---

## 🛠️ Tech Stack
- Databricks
- Apache Spark (PySpark)
- Delta Lake
- SQL
- Power BI
- GitHub

---

## Dataset
- **Source:** 1. https://developer.imdb.com/non-commercial-datasets/
- 2. https://help.imdb.com/article/contribution/other-submission-guides/country-codes/G99K4LFRMSC37DCN#
  3. https://en.wikipedia.org/wiki/List_of_ISO_639_language_codes
- 

---

## 🚀 Key Learnings
- Dimensional data modeling
- Medallion architecture
- Star schema & bridge tables
- BI optimization for DirectQuery
- Translating business requirements into analytics

---

## ✅ Conclusion
This project demonstrates a production-style analytical data warehouse built using modern data engineering and BI best practices.


