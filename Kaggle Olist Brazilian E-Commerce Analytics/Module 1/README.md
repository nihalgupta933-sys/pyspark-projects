# 🔍 Module 1: Data Ingestion & Exploratory Data Analysis

This module covers the cluster-level data ingestion process via SSH into the Hadoop Distributed File System (HDFS) and the initial Exploratory Data Analysis (EDA) using PySpark to profile schemas, columns, and data types.

---

## 🏗️ Data Ingestion & Cluster Setup

In a production environment, data processing is offloaded to multi-node clusters rather than local machines. For this project, the dataset was ingested and staged onto a cloud infrastructure environment using the following steps:

1. **Secure Shell (SSH) Access:** Connected directly to the cloud master node instance using terminal credentials.
2. **Directory Initialization:** Created a dedicated workspace environment on the cluster file system:
   ```bash
   mkdir -p olist/data && cd olist/data
   ```
3. **Data Acquisition:** Downloaded the zipped source files directly using curl commands via the official API endpoint, or manually staged via secure copy protocol (SCP).
   * **Dataset Source:** You can find and download the source dataset directly from the official link here: [Kaggle Olist Brazilian E-Commerce Public Dataset](https://kaggle.com).
4. **Decompression:** Extracted the flat `.csv` target files into the staging folder:
   ```bash
   unzip brazilian-ecommerce.zip -d ~/olist/data/
   ```
5. **HDFS Migrations:** Transferred the unzipped flat files from local cluster block storage straight into the distributed HDFS layer using standard Hadoop system commands:
   ```bash
   hadoop fs -put ~/olist/data/*.csv /user/hadoop/olist/
   ```

With the files successfully loaded into the distributed cluster file system, a PySpark `SparkSession` was initialized inside a Jupyter Notebook to begin distributed analysis.

![Spark Session Initialization](./ss/Screenshot%202026-08-03%20132512.png)

---

## 📊 Distributed Exploratory Data Analysis (EDA)

Once the raw data files were available in HDFS, the PySpark DataFrame API was used to profile structural integrity, shapes, and distributions without execution outputs saved inline.

### 📁 1. Initial Ingestion Verification
The flat relational tables were parsed from CSV lines directly out of HDFS. Initial data frames were verified using the `.show()` action to inspect text alignment and columns.
![Data Frame Loading View](./ss/Screenshot%202026-08-03%20132626.png)

### 📋 2. Relational Schema & Type Profiling
Structural structural formats were verified for core entities like `orders` and `customers`. Printouts confirm explicit field data types (Strings, Timestamps, Integers) and structural nullability constraints.
![Orders and Customers Schema Printouts](./ss/Screenshot%202026-08-03%20132658.png)

### 🆔 3. Primary Key & Integrity Checks
Primary identifiers and critical fields were profiled across frames using distinct-count metrics. This phase evaluated data integrity, uncovered natural primary keys, and flagged duplicate entry metrics.
![Data Deduplication & Key Profiling](./ss/Screenshot%202026-08-03%20132744.png)

### 🗺️ 4. Geographic Demographics & Status Distributions
Data rows were aggregated to isolate geographic volume variations. Order records were segmented by customer state location alongside a clean distribution table showing absolute statuses (`delivered`, `shipped`, `canceled`).
![State-wise Demographics & Order Status Distributions](./ss/Screenshot%202026-08-03%20132828.png)

### 💳 5. Financial Transaction Profiling
Aggregations run on the payment datasets map consumer transaction profiles. The analysis highlights common transaction formats (Credit Cards, Vouchers, *Boleto*) along with financial value metrics.
![Payment Methods & Transaction Metrics Analysis](./ss/Screenshot%202026-08-03%20132915.png)

### 📦 6. Product Category Volume Analysis
Order lines were matched to isolate product categorization rankings. Top-selling product segments were generated to pinpoint product types that drive the highest retail order quantities.
![Top Selling Retail Items Optimization](./ss/Screenshot%202026-08-03%20132942.png)

### 🚚 7. Logistics Turnaround & Delivery Latencies
Calculations were run on shipment timestamps to compute physical fulfillment turnaround rates. This analysis profiles the historical average delivery durations across the regional logistics footprint.
![Average Delivery Duration Latency Performance](./ss/Screenshot%202026-08-03%20133023.png)

