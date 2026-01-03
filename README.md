Snowflake Analytics Engineering Pipeline with dbt and Airflow

Overview
This project demonstrates a production style analytics engineering ELT pipeline built using Snowflake, dbt, and Apache Airflow (Astro runtime).
The goal of the project is to show how raw warehouse data can be transformed into analytics ready fact and dimension tables using dbt, with workflow orchestration handled by Airflow.
The pipeline follows modern analytics engineering best practices including layered data modeling, automated data quality checks, and orchestration ready execution.

Tech Stack

Snowflake – Cloud data warehouse

dbt Core – Analytics engineering and transformations

Apache Airflow – Workflow orchestration

Astro CLI – Local Airflow runtime

Docker – Containerized execution

Python – DAG definitions

Architecture
Snowflake (TPCH sample data)
        ↓
dbt Sources
        ↓
Staging Models
        ↓
Intermediate Models
        ↓
Mart Models (Fact Tables)
        ↓
Analytics Ready Tables

Airflow is used to orchestrate dbt runs in a production like environment.

dbt Implementation

The dbt project uses Snowflake’s TPCH sample dataset as the source.

Key Features

Source definitions with freshness checks
Staging models with clean naming conventions
Fact tables built for analytics use cases
Reusable dbt macros
Automated data quality tests
Dependency management using dbt packages

Typical dbt commands used:

dbt deps
dbt build
dbt test

Airflow Orchestration

Apache Airflow is run locally using Astro CLI, providing a production like orchestration environment.

