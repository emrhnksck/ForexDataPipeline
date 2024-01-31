
# Forex Data Pipeline 

This repository contains a Python script for a simple data pipeline using Apache Airflow to fetch, process, and store forex rates data.

## Pipeline Steps:
### Download Forex Rates:

Checks API availability using an HTTP sensor.
Verifies the existence of forex_currencies.csv.
Downloads forex rates for specified pairs and stores them in forex_rates.json.

### Save Rates to HDFS:

Uses a BashOperator to save forex_rates.json to HDFS in the /forex directory.

### Create Hive Table:

Defines an external Hive table (forex_rates) with columns for base, last_update, and rates for specific currencies.

### Spark Processing:

Submits a Spark application (forex_processing.py) for additional data processing. The script content is not provided.

### Email Notification:

Sends an email notification upon pipeline completion to emrehan@yopmail.com.

![image](https://github.com/emrhnksck/ForexDataPipeline/assets/58311722/038e6c4a-dba8-4325-81f0-7b0c2a313e09)
