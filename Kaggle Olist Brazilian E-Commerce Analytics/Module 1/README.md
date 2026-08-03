# 🔍 Module 1: Data Exploration

This module shows how to get the Olist data, move it into the cloud cluster system, and explore it using PySpark.

👉 [Click Here to View the Module 1 Code Notebook](./Module%201%20-%20Data%20Exploration.ipynb)

---

## 🏗️ Step 1: Getting the Data and Setting up HDFS

In real projects, we use a cloud cluster system (like GCP Dataproc) instead of our own laptops. Here is how the data was uploaded in the background using terminal commands (SSH):

1. **Created Folders:** Opened the cluster terminal and used `mkdir olist` to create a project directory.
2. **Downloaded Data:** Downloaded the Brazilian e-commerce files directly onto the cluster. You can find the raw files here: [Kaggle Olist Brazilian E-Commerce Public Dataset](https://kaggle.com).
3. **Unzipped Files:** Extracted the flat files into a subfolder named `data`.
4. **Moved to HDFS:** Used `hadoop fs -put` commands to transfer all the unzipped CSV files from the local cluster storage directly into the distributed HDFS file system.

Once the data was safely in HDFS, a PySpark session was started inside a Jupyter Notebook to begin looking at the data:

![Spark Session Setup](./ss/Screenshot%202026-08-03%20132512.png)

---

## 📊 Step 2: Looking at the Data

Here are the step-by-step screenshots showing exactly what was analyzed in the notebook:

### 📁 Reading the CSV Files
This step reads the raw data from the CSV files stored in HDFS and displays the rows on the screen.
![Read CSV data](./ss/Screenshot%202026-08-03%20132626.png)

### 📋 Checking Table Schemas
This step prints out the column structures and data types for the orders and customers tables.
![Print table schemas](./ss/Screenshot%202026-08-03%20132658.png)

### 🆔 Checking Duplicate Values
This step explores the dataset to find duplicate records and check critical data fields.
![Explore duplicates and fields](./ss/Screenshot%202026-08-03%20132744.png)

### 🗺️ Customers and Orders Distribution
This step checks how many customers belong to each Brazilian state, along with the distribution of different order statuses.
![Customer state and order status distributions](./ss/Screenshot%202026-08-03%20132828.png)

### 💳 Payment Analysis
This step explores the payments dataset to see how customers chose to pay for their orders.
![Explore payments](./ss/Screenshot%202026-08-03%20132915.png)

### 📦 Top Selling Items
This step filters and counts the dataset rows to find out which items are the top sellers.
![Explore top selling items](./ss/Screenshot%202026-08-03%20132942.png)

### 🚚 Delivery Time Analysis
This step calculates dates and numbers to analyze the average time it takes for orders to be delivered.
![Average delivery time analysis](./ss/Screenshot%202026-08-03%20133023.png)
