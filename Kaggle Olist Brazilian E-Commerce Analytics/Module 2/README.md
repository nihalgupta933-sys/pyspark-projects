# 🧹 Module 2: Data Cleaning & Transformation

This module covers the steps taken to handle missing data, clean column formats, transform features, and save the clean results using PySpark.

👉 [Click Here to View the Module 2 Code Notebook](./Module%202%20-%20Data%20Cleaning%20%26%20Transformation.ipynb)

---

## 🛠️ Step-by-Step Data Cleaning Process

Here are the step-by-step screenshots showing exactly what was done in the notebook:

### 🔍 Checking for Missing Values
This step checks the `orders`, `customers`, and `order_items` tables to find out which columns contain missing (null) values.
![Check missing values](./ss/Screenshot%202026-08-03%20133359.png)

### 🧹 Handling and Filling Missing Values
This step processes the missing values found in the datasets and fills them using cleaning rules.
![Handle and fill missing values](./ss/Screenshot%202026-08-03%20133448.png)

### 🔢 Imputing Missing Values
This step uses imputation techniques to replace empty cells with appropriate default values or metrics.
![Impute missing values](./ss/Screenshot%202026-08-03%20133520.png)

### 📋 Custom Function for Schema Printing
This step defines a custom helper function to automatically print and verify the data types and column structures across the notebooks.
![Custom function for schema printing](./ss/Screenshot%202026-08-03%20133556.png)

### 💳 Cleaning Payment Types
This step cleans up the payment method column to make sure all payment types are uniform and spelled correctly.
![Clean payment types](./ss/Screenshot%202026-08-03%20133630.png)

### 🧼 Additional Data Cleaning
This step performs more cleaning tasks to remove bad rows and fix formatting errors across the remaining tables.
![More data cleaning](./ss/Screenshot%202026-08-03%20133726.png)

### ⚡ Advanced Transformation
This step runs advanced DataFrame transformations to modify values and prepare columns for deeper calculations.
![Advanced data transformation](./ss/Screenshot%202026-08-03%20133849.png)

### 📊 Printing Clean Data Summary
This step prints out the freshly cleaned DataFrames along with statistical summaries to confirm the data is accurate.
![Print clean data summary](./ss/Screenshot%202026-08-03%20133924.png)

### 📦 Product and Payment Transformations
This step transforms product dimensions and category text while printing out a finalized, clean view of the payments dataset.
![Product and payment transformations](./ss/Screenshot%202026-08-03%20133954.png)

### 💰 Total Revenue Per Customer
This step aggregates order costs and values together to calculate exactly how much money each unique customer spent.
![Total revenue per customer](./ss/Screenshot%202026-08-03%20134017.png)

### 💾 Saving Clean Data as Parquet in HDFS
This final step exports the clean datasets out of memory and saves them into the distributed HDFS file system as optimized Parquet files.
![Store clean data as Parquet in HDFS](./ss/Screenshot%202026-08-03%20134103.png)
