# Clinical Database Analytics & Applied Computing

[![Database](https://img.shields.io/badge/Database-SQL%20%7C%20PostgreSQL-336791.svg)](https://www.postgresql.org/)
[![Computing](https://img.shields.io/badge/Computing-Python%203.9+-3776AB.svg)](https://www.python.org/)
[![Data Processing](https://img.shields.io/badge/Data%20Eng-Pandas%20%7C%20NumPy-150458.svg)](https://pandas.pydata.org/)
[![Standards](https://img.shields.io/badge/Clinical%20Models-EHR%20%7C%20OMOP%20CDM-red.svg)](https://www.ohdsi.org/)

This module covers clinical database architecture, enterprise relational querying, and applied Python computation for healthcare data. It bridges raw transactional Electronic Health Record (EHR) schemas with analytical data modeling for clinical decision support, cohort identification, and quality metrics reporting.

---

## Technical Competencies & Toolsets

| Domain Area | Tools & Frameworks | Applied Clinical Methodologies |
| :--- | :--- | :--- |
| **Relational Clinical Querying** | SQL, PostgreSQL, SQLite, MySQL | Multi-table relational joins, Common Table Expressions (CTEs), subqueries, and window functions applied across clinical encounter tables. |
| **Cohort & Quality Extraction** | ANSI SQL, Aggregations, GROUP BY | Constructing complex patient cohorts, 30-day readmission flags, length-of-stay (LOS) metrics, and healthcare utilization indicators. |
| **Applied Clinical Computing** | Python (Pandas, NumPy) | Automated data ingestion, handling missing clinical variables, normalization pipelines, and structured export for downstream reporting. |
| **Schema & Data Standards** | Relational Schemas, Data Dictionaries | Querying normalized EHR tables (Patients, Encounters, Conditions, Lab Observations) and mapping toward common data models (OMOP CDM). |

---

## Core Focus Areas

### 1. Relational Healthcare Architecture & Query Optimization
* **Cohort Extraction:** Writing modular SQL statements using CTEs to isolate complex chronic disease cohorts based on multi-criteria encounter criteria.
* **Clinical Aggregations:** Calculating hospital census trends, bed turnover rates, and longitudinal patient encounter frequencies using window functions (`ROW_NUMBER()`, `RANK()`, `PARTITION BY`).
* **Integrity & Constraints:** Enforcing referential constraints and handling longitudinal EHR nuances, such as ambiguous null values, date calculations, and duplicate claim records.

### 2. Python-Driven Healthcare Pipelines
* **ETL Workflows:** Transforming tabular data extracts from relational databases into analysis-ready formats using Pandas.
* **Data Hygiene:** Addressing clinical data anomalies, date-time formatting standardizations across varying time zones, and handling missing laboratory panels.
* **Interoperable Exports:** Bridging SQL database outputs with downstream interoperability pipelines (converting query results into serialized formats such as JSON).

---

## Applied Objectives
* Execute optimized relational queries against transactional and analytical clinical databases.
* Apply Python for reproducible clinical data pipelines, validation, and automated reporting.
* Prepare for and demonstrate applied competencies required in clinical analytics certifications and enterprise healthcare systems.
