# 🔗 Module 3: Data Integration & Aggregation

This module focuses on combining multiple tables together using PySpark DataFrames and running aggregations to calculate important business metrics.

👉 [Click Here to View the Module 3 Code Notebook](./Module%203%20-%20Data%20Integration%20%26%20Aggregation%20.ipynb)

---

## 🛠️ Step-by-Step Data Integration & Aggregation Process

Here are the step-by-step screenshots showing exactly what was done in the notebook:

### 🔗 Optimized Table Joins
This step performs optimized table joins to connect different parts of the dataset together for deep data integration.
![Optimized table joins](./ss/Screenshot%202026-07-30%20135429.png)

### 📊 Ingestion Aggregations
This step applies basic group-by operations and counts to summarize the records across the combined tables.
![Basic aggregations](./ss/Screenshot%202026-07-30%20135447.png)

### 🏆 Top Products and Spending Customers
This step calculates and finds the most sold items along with the top 10 customers who spent the most money.
![Top items and buyers](./ss/Screenshot%202026-07-30%20135502.png)

### 🪟 Window Functions and Ranking
This step uses Spark window functions to sort data rows and assign ranks based on specific features.
![Window functions ranking](./ss/Screenshot%202026-07-30%20135520.png)

### ⚡ Advanced Aggregation
This step runs more advanced calculations across multiple columns to generate multi-level summary metrics.
![Advanced calculations](./ss/Screenshot%202026-07-30%20135532.png)

### 📈 Merchant Performance Metrics
This step analyzes merchant metrics to see which partners generate the highest sales volumes and cleanest fulfillment rates.
![Merchant performance](./ss/Screenshot%202026-07-30%20135543.png)

### 📦 Product Popularity Metrics
This step ranks product categories based on order frequencies to show popularity trends over time.
![Product popularity](./ss/Screenshot%202026-07-30%20141724.png)

### 📅 Monthly Sales Revenue and Order Counts
This step groups order records by months to track continuous revenue patterns and total order volumes.
![Monthly revenue records](./ss/Screenshot%202026-07-30%20144142.png)

### 🔄 Customer Retention Metrics
This step tracks historical repeat buyer frequencies to measure the exact customer retention rates.
![Customer retention checks](./ss/Screenshot%202026-07-30%20145427.png)

### 📑 Extended Schema Enrichment
This step builds new conditional columns and flag features to enrich the core dataset tables.
![Extended schema enrichment](./ss/Screenshot%202026-07-31%20123500.png)

### 💰 Order Revenue Calculations
This step combines individual item prices, values, and quantities to calculate the final absolute revenue per order.
![Order revenue math](./ss/Screenshot%202026-07-31%20124059.png)

### 👥 Customer Spending Segmentation
This step segments individual buyer records into distinct tiers based on their total historical spending habits.
![Customer segmentation tiers](./ss/Screenshot%202026-07-31%20125657.png)

### 📅 Weekday vs. Weekend Analysis
This step splits order volumes apart to compare consumer shopping habits on weekdays versus weekends.
![Weekday vs weekend shopping habits](./ss/Screenshot%202026-07-31%20135505.png)

### 🚚 Freight Cost Analysis
This step analyzes localized shipping expenses and delivery freight fees across different purchase weights.
![Freight cost analysis](./ss/Screenshot%202026-07-31%20140239.png)

### 🗺️ Order Volume by State
This step groups all final order distributions by unique customer states to locate the top purchasing regions across Brazil.
![Order volumes grouped by state](./ss/Screenshot%202026-07-31%20140806.png)

