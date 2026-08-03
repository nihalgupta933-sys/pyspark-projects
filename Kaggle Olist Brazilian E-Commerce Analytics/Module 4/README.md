# ⚡ Module 4: Spark Configuration Optimization

This module covers tuning configurations for a Google Cloud Platform (GCP) Dataproc cluster and applying optimized join strategies to make code run faster.

👉 [Click Here to View the Module 4 Code Notebook](./Module%204%20-%20Spark%20Configuration%20Optimization.ipynb)

---

## 🛠️ Step-by-Step Optimization Process

Here are the screenshots showing exactly what optimization steps were done in the notebook:

### ⚙️ 1. Cluster Setup & Memory Configurations
This step outlines the GCP Dataproc cluster specs (8 worker vCPUs and 32 GB RAM total) and configures memory settings like `spark.executor.memory` (6G) and `spark.driver.memory` (4G) inside the SparkSession initialization block.
![Cluster resource planning and memory tuning](./ss/Screenshot%202026-08-01%20192410.png)

### 📥 2. HDFS Ingestion & Stage Execution Tracking
This step tracks active cluster stage boundaries (`Stage 0`, `Stage 1`, etc.) while pulling the flat relational CSV files out of distributed HDFS storage paths.
![Data ingestion and stage execution metrics](./ss/Screenshot%202026-08-01%20192429.png)

### 🔀 3. Advanced Optimized Join Strategies
This step tests advanced Spark execution patterns to handle skewed data structures efficiently:
* **Broadcast Join:** Broadening smaller lookups (`broadcast(customers_df)`) to skip expensive shuffles.
* **Sort-Merge Join:** Presorting table rows locally inside partition ranges (`sortWithinPartitions`).
* **Bucket Join:** Repartitioning parallel streams (`repartition(10, 'customer_id')`) to prevent uneven cluster workloads.
![Optimized table join strategies](./ss/Screenshot%202026-08-01%20192447.png)

