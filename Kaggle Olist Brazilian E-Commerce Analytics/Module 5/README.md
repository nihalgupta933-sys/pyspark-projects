# 💾 Module 5: Data Serving Layer

This module focuses on saving and retrieving processed analytical data efficiently using multi-format storage approaches like Parquet, Hive, and CSV inside the GCP Dataproc environment.

👉 [Click Here to View the Module 5 Code Notebook](./Module%205%20-%20Data%20Serving%20Layer.ipynb)

---

## 🛠️ Step-by-Step Data Serving Process

Here are the screenshots showing exactly how the final analytical datasets were stored and made ready for production use:

### 🎯 1. Module Objective & Configurations
This step initializes the tuned cluster-backed `SparkSession` to handle large exports and defines the main goals: saving data efficiently using multiple storage frameworks for downstream consumption.
![Data serving objectives and session configs](./ss/Screenshot%202026-08-01%20201146.png)

### 💾 2. Storing Data in HDFS & Google Cloud Storage (GCS)
This step checks directory listings using Hadoop commands, reads the processed data, and saves it in two places:
* **HDFS Parquet Export:** Saved directly into Hadoop distributed paths using `.write.mode('overwrite').parquet('/data/serve')`.
* **Cloud Object Storage (GCS Bucket):** Saved securely to a permanent cloud bucket using Google Cloud Storage paths (`gs://dataproc-staging...`).
![Storing as Parquet in HDFS and GCS storage buckets](./ss/Screenshot%202026-08-01%20201226.png)

### 🗄️ 3. Storing as Hive Tables & CSV Formats
This step completes the pipeline by exposing data to relational engines and analytics tools:
* **Hive Metastore Tables:** Stored as an organized database table using `.saveAsTable('cleaned_data')` and verified with `spark.sql('show tables')`.
* **Standard CSV Export:** Written out with explicit headers to standard `/data/tem/` CSV directories for quick dashboarding connections.
![Storing as persistent Hive tables and flat CSV lines](./ss/Screenshot%202026-08-01%20201241.png)

