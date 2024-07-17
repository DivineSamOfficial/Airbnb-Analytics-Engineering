# Airbnb Analytics Engineering and Data Ware housing 

## Project Overview
This project involves ingesting Airbnb data into Amazon S3, transforming it using Snowflake and dbt, orchestrating workflows with Dagster, and visualizing data with Preset.

## Architecture
![Architecture Diagram](https://github.com/DivineSamOfficial/Airbnb-Anlaytics-Engineering/blob/main/Sys%20Arch.jpg)

## DAG
![DAG](https://github.com/DivineSamOfficial/Airbnb-Anlaytics-Engineering/blob/main/DAG.png)

## Lineage Graph
![lineage Graph](https://github.com/DivineSamOfficial/Airbnb-Anlaytics-Engineering/blob/main/Lineage%20Graph.png)

## Dashboard
![Dashboard](https://github.com/DivineSamOfficial/Airbnb-Anlaytics-Engineering/blob/main/Dashboard.jpg)

## Implementation Details

### Data Pipeline
- **Data Ingestion:** Airbnb data is ingested into Amazon S3.
- **Data Transformation:** Processed in Snowflake using dbt.
  - Materialized data into views, tables, incremental, and ephemeral models.
  - Checked staleness of data by maintaining source data and scheduling tests.
  - Implemented SCD type 2 with dbt snapshots.
  - Created generic and custom tests using dbt macros.
  - Comprehensive documentation with dbt docs.
  - Managed table permissions with dbt hooks.
  - Documented dashboards with dbt exposure.
  - Advanced testing using dbt expectations framework.

### Orchestration
- **Pipeline Orchestration:** Implemented with Dagster.
  - Partitioned incremental models for performance optimization and backfilling.
  - Job scheduling for automated workflows.

### Visualizations
- **Preset:** Used for data visualization and dashboarding.

## Tools Used
- **Snowflake**: Data warehousing
- **dbt**: Data transformation and testing
- **Dagster**: Pipeline orchestration
- **Amazon S3**: Data storage
- **Preset**: Data visualization

## Setup and Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
