
# 🚀 Data Engineering Portfolio: PySpark Projects

Welcome to my PySpark portfolio! This repository contains end-to-end data processing pipelines implemented using Apache Spark on cloud architecture.

---

## 📁 Project 1: Mini Customer Data Pipeline (1,000 Records)
An end-to-end PySpark mini-project implemented on GCP to read, process, multi-join, and analyze a dataset of 1,000 customers.

### 📝 Code File
*   [View Jupyter Notebook (`MiniProject1.ipynb`)](./MiniProject1.ipynb)

### 📈 Step-by-Step Execution Outputs
Below is the sequential pipeline execution captured directly from the GCP cluster environment:

#### **Phase 1: Environment Setup & Data Ingestion**
*   **Step 1: Basic Creation of Spark Session & Data Ingestion**
    ![Spark Session & Read](ss/Screenshot%202026-07-25%20154344.png)
*   **Step 2: Pivot Table Analysis - Count of Active & Inactive Users per State**
    ![Pivot Table Active/Inactive](ss/Screenshot%202026-07-25%20154427.png)

#### **Phase 2: Core Data Transformations & Customer Profiles**
*   **Step 3: Temporal Analysis - Finding Closest Registration Dates**
    ![Closest Registration](ss/Screenshot%202026-07-25%20154706.png)
*   **Step 4: Demographic Extremes - Oldest and Newest Customer per City**
    ![Oldest & Newest per City](ss/Screenshot%202026-07-25%20154732.png)

#### **Phase 3: Relational Joins & Transactional Analysis**
*   **Step 5: Joining & Analyzing Customer and Order Datasets**
    ![Customer & Order Join](ss/Screenshot%202026-07-25%20154748.png)
*   **Step 6: Comprehensive Analysis of Order Metrics**
    ![Order Analysis](ss/Screenshot%202026-07-25%20154821.png)
*   **Step 7: Applying Multi-Key Relational Joins**
    ![Applying Joins](ss/Screenshot%202026-07-25%20154837.png)

#### **Phase 4: Business Intelligence & Aggregated Metrics**
*   **Step 8: Revenue Aggregations - Total Order and Spend per Customer**
    ![Total Orders & Spend](ss/Screenshot%202026-07-25%20154915.png)
*   **Step 9: Financial Benchmarks - Average Spend by Customer**
    ![Average Spend](ss/Screenshot%202026-07-25%20154947.png)

#### **Phase 5: Advanced Analytics & Customer Segmentation**
*   **Step 10: Advanced Analytics - Window Operations & Ranking**
    ![Window Operation](ss/Screenshot%202026-07-25%20155126.png)
*   **Step 11: Anomaly Detection - Customers with High Order Frequency but Low Spend**
    ![High Freq Low Spend Segment](ss/Screenshot%202026-07-25%20155148.png)

---

## 📁 Project 2: Kaggle Olist Brazilian E-Commerce Analytics
*(⏳ Setting up soon — This project will involve advanced analytics on the large scale Olist e-commerce dataset using PySpark)*
