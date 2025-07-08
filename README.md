# ETL-Pipeline-with-Airflow
 ## 📌 Overview

This repository contains a project-based ETL pipeline built using Apache Airflow (pre-Airflow 3 version), designed to reflect a real-world workflow. The pipeline extracts user data from a public API, transforms it into a structured format using pandas, and loads it into a PostgreSQL database.

This project highlights the use of Airflow’s classic operators and demonstrates how to build and schedule a multi-step workflow that integrates external APIs and databases.

## 🎯 Project Objectives

- Build a DAG that mimics a real-world ETL workflow
- Automate data ingestion from an external API
- Perform data transformation and normalization using Python and pandas
- Store the cleaned data in a PostgreSQL database
- Apply core Airflow concepts: task orchestration, sensors, hooks, and XComs

---

## 🧰 Tools & Technologies

- **Apache Airflow** (classic operators)
- **Python 3**
- **PostgreSQL**
- **Pandas**
- **Airflow Providers:**
  - `postgres`
  - `http`
---

## 📁 Project Structure

.
├── user_processing.py # Main DAG file
└── /tmp/processed_user.csv # Generated output file (runtime)
└── README.md                # Project documentation

---

## 📝 Notes

- This project was implemented using Airflow’s classic syntax (prior to version 3).
- Data is shared between tasks using Airflow's `XCom` mechanism.
- The API (`randomuser.me`) returns synthetic user data. Without deduplication, repeated DAG runs may cause duplicate entries in the database.

