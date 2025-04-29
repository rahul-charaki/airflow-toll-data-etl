# ETL Toll Data Airflow DAG

This project contains an Apache Airflow DAG for processing toll data from different toll plazas. The DAG performs the following steps:

1. Downloads the dataset.
2. Extracts data from CSV, TSV, and fixed-width files.
3. Consolidates and transforms the data into a single CSV file.
4. Loads the transformed data into a staging area.

## Requirements

- Apache Airflow 2.4.1 or higher
- Python 3.9 or higher
- Additional Python libraries (listed in `requirements.txt`)

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/rahul-charaki/airflow-toll-data-etl
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Copy the DAG file to your Airflow DAGs directory:
   ```bash
   cp ETL_toll_data.py $AIRFLOW_HOME/dags/
   ```

4. Start the Airflow web server and scheduler:
   ```bash
   airflow webserver
   airflow scheduler
   ```

## Running the DAG

The DAG will run daily as per the schedule set in the `ETL_toll_data.py` file.

