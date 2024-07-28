# Data_Warehouse_Management

# Overview
This project involves creating an Apache Airflow DAG to automate the loading of logistics data into a Hive database on GCP Dataproc. The system ensures data is loaded efficiently and archived appropriately.

# Features
 -GCS Sensor: Detects new files in the logistics raw data bucket.
 -Hive Database and Tables: Creates Hive database and tables, including partitioned tables.
 -Dynamic Partitioning: Configures dynamic partitioning in Hive.
 -Data Archival: Moves processed files to an archive bucket.
 
 # DAG Components
-sense_logistics_file: GCSObjectsWithPrefixExistenceSensor to detect new files.
-create_hive_database: Creates Hive database if it doesn't exist.
-create_hive_table: Creates the main Hive table.
-create_partitioned_table: Creates a partitioned Hive table.
-set_hive_properties_and_load_partitioned: Sets Hive properties and loads data into the partitioned table.
-archive_processed_file: Moves processed files to an archive bucket.

# Architecture Daigram

![architecture](https://github.com/user-attachments/assets/e18eb209-8c16-4332-a0f7-3f17a8163ee7)
