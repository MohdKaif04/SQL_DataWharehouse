# 🏗️ SQL Data Warehouse Project

A modern SQL Server Data Warehouse built using **T-SQL, ETL workflows, and Medallion Architecture** to transform raw data into clean, structured, and analytics-ready datasets.

The project demonstrates how to organize a data warehouse using **Bronze, Silver, and Gold layers**, implement reusable SQL loading procedures, perform data quality checks, and prepare data for business reporting and analysis.

## 📌 Project Overview

This project focuses on building a structured data warehouse using SQL Server. It includes database initialization, data ingestion, data transformation, dimensional modeling, and validation scripts.

The goal is to create a reliable data pipeline that converts raw source data into organized, consistent, and analysis-ready data.

### 🎯 Project Objectives

- Design a structured SQL Server data warehouse.
- Implement a layered data processing architecture.
- Build reusable SQL scripts and stored procedures for data loading.
- Clean, standardize, and transform raw data.
- Apply data quality checks to validate processed data.
- Organize business-ready data using dimensional modeling concepts.

## 🏛️ Architecture

This project follows the **Medallion Architecture**.

| Layer | Purpose |
|---|---|
| 🥉 Bronze | Stores raw source data with minimal transformation. |
| 🥈 Silver | Cleans, standardizes, and transforms data for consistency. |
| 🥇 Gold | Organizes processed data into business-ready structures for analytics. |

### 🔄 Data Processing Flow

`Source Data → Bronze Layer → Silver Layer → Gold Layer → Analytics`

Each layer has a distinct responsibility, making the pipeline easier to understand, maintain, and validate.

## 🛠️ Tech Stack

- **Database:** Microsoft SQL Server
- **Query Language:** T-SQL
- **Data Engineering:** ETL, data transformation, stored procedures
- **Data Architecture:** Medallion Architecture (Bronze, Silver, Gold)
- **Data Modeling:** Dimensional modeling and Star Schema concepts
- **Data Validation:** SQL-based data quality checks
- **Version Control:** Git and GitHub

## 📂 Project Structure

```text
SQL_DataWharehouse/
│
├── datasets/                         # Source datasets
│
├── scripts/
│   ├── init_database.sql              # Database initialization
│   │
│   ├── bronze/
│   │   ├── ddl_bronze.sql             # Bronze table definitions
│   │   └── proc_load_bronze.sql       # Bronze data loading procedure
│   │
│   ├── silver/
│   │   ├── ddl_silver.sql             # Silver table definitions
│   │   └── proc_load_silver.sql       # Silver transformation/loading
│   │
│   └── gold/
│       └── ddl_gold.sql               # Gold layer definitions
│
├── tests/
│   ├── quality_checks_silver.sql      # Silver layer validations
│   └── quality_checks_gold.sql        # Gold layer validations
│
├── .gitignore
├── LICENSE
└── README.md
```

## ⚙️ Key Features

### 1. Database Initialization
SQL scripts establish the database environment and prepare the objects required for data processing.

### 2. Bronze Layer — Raw Data Ingestion
Defines the raw data structures and provides a reusable procedure for loading source data into the Bronze layer.

### 3. Silver Layer — Data Cleaning and Transformation
Uses SQL scripts and loading procedures to process data and prepare it for downstream analysis.

### 4. Gold Layer — Analytics-Ready Data
Defines the final layer for organizing processed data into business-oriented structures that support analytical queries and reporting.

### 5. Data Quality Checks
Includes dedicated SQL scripts for validating data quality and checking the processed data in the Silver and Gold layers.

### 6. Modular SQL Design
Separates database initialization, layer definitions, loading logic, and testing into individual scripts for easier maintenance.

## 🚀 Getting Started

### Prerequisites

- Microsoft SQL Server
- SQL Server Management Studio (SSMS)
- Git
- Project source datasets

### Step 1: Clone the Repository

```bash
git clone https://github.com/MohdKaif04/SQL_DataWharehouse.git
```

Navigate to the project directory:

```bash
cd SQL_DataWharehouse
```

### Step 2: Configure the Dataset Paths

Ensure the required source dataset files are available in the `datasets/` directory.

If the SQL loading procedure uses local file paths, update those paths in `scripts/bronze/proc_load_bronze.sql` to match your local dataset location and SQL Server's file access permissions.

### Step 3: Initialize the Database

Open SSMS, connect to your SQL Server instance, and execute:

```text
scripts/init_database.sql
```

### Step 4: Create the Bronze Layer

Execute:

```text
scripts/bronze/ddl_bronze.sql
```

Then execute the Bronze loading procedure definition:

```text
scripts/bronze/proc_load_bronze.sql
```

Run the procedure using the name defined in the script.

### Step 5: Create and Load the Silver Layer

Execute the Silver layer definition:

```text
scripts/silver/ddl_silver.sql
```

Then execute:

```text
scripts/silver/proc_load_silver.sql
```

Run the loading procedure using the name defined in the script.

### Step 6: Build the Gold Layer

Execute:

```text
scripts/gold/ddl_gold.sql
```

This prepares the Gold layer objects defined by the project.

### Step 7: Run Data Quality Checks

Execute the validation scripts:

```text
tests/quality_checks_silver.sql
tests/quality_checks_gold.sql
```

Review the results to identify potential data quality issues.

> **Note:** Run the scripts in the appropriate order. Review database names, file paths, and any destructive SQL statements before executing them.

## 📚 Key Concepts Demonstrated

- SQL Server database development
- ETL pipeline design
- T-SQL scripting
- Stored procedures
- Data cleaning and standardization
- Bronze, Silver, and Gold data layers
- Dimensional modeling concepts
- Data quality validation
- Git-based version control

## 💡 What I Learned

Through this project, I practiced organizing a data warehouse into separate processing layers, writing modular SQL scripts, implementing reusable data-loading logic, and validating processed data using SQL.

The project strengthened my understanding of how raw source data can be structured and prepared for reliable downstream analytics.

## 🔮 Future Improvements

- Add automated pipeline execution and scheduling.
- Improve error handling and logging for data-loading procedures.
- Expand data quality checks and validation rules.
- Document the warehouse schema and data lineage.
- Integrate a BI tool for interactive reporting and dashboards.

## 👨‍💻 Author

**Mohd Kaif**

- GitHub: [@MohdKaif04](https://github.com/MohdKaif04)
- Project Repository: [SQL Data Warehouse](https://github.com/MohdKaif04/SQL_DataWharehouse)

---

⭐ If you find this project useful, consider giving the repository a star.

**Built with SQL Server and T-SQL.**
