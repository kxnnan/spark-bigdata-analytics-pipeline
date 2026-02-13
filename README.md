# 🚀 Spark Big Data Analytics Pipeline

## 📌 Project Overview

This project demonstrates a scalable Apache Spark-based Big Data Analytics pipeline processing **1M+ synthetic sales records**.

The pipeline includes:

- Batch data processing using PySpark
- Manual schema definition (production-ready ingestion)
- Revenue aggregation and customer analytics
- Window functions with ranking
- Performance benchmarking (cache vs non-cache)
- Partitioned Parquet storage
- Structured Streaming (real-time processing simulation)

This project showcases distributed data processing and performance optimization techniques used in real-world Data Engineering systems.

---

## 🧱 Architecture Flow

CSV Data  
↓  
Spark Ingestion (Manual Schema)  
↓  
Data Transformation (withColumn, Aggregations)  
↓  
Window Functions (Customer Ranking per Country)  
↓  
Partitioned Parquet Storage (Data Lake Style)  
↓  
Structured Streaming (Micro-batch Processing)

---

## 🔥 Key Features

### ✅ 1. Manual Schema Definition
- Avoided `inferSchema`
- Production-ready ingestion
- Improved loading performance

### ✅ 2. Large Dataset Processing
- Generated and processed 1M+ records
- Demonstrated distributed computation

### ✅ 3. Revenue Calculation
Created computed column:
TotalPrice = Amount × Quantity

### ✅ 4. Aggregation
- Country-level revenue calculation
- Customer-level revenue aggregation

### ✅ 5. Window Functions
- Ranked customers per country using:
  - `partitionBy`
  - `orderBy`
  - `rank()`

### ✅ 6. Performance Optimization
- Compared execution time:
  - Without cache
  - With cache
- Observed impact of distributed execution and memory caching

### ✅ 7. Partitioned Parquet Storage
Stored processed data using:
.partitionBy("Country")

Improves:
- Query performance
- Data lake organization
- Parallel reads

### ✅ 8. Structured Streaming
Implemented micro-batch streaming using:
readStream → transform → groupBy → writeStream

Demonstrates real-time analytics pipeline behavior.

---

## 🛠 Technologies Used

- Apache Spark (PySpark)
- Python
- Pandas
- NumPy
- Matplotlib

---

## ⚡ Performance Concepts Demonstrated

- Lazy Evaluation
- Narrow vs Wide Transformations
- Shuffle Operations
- Hash Aggregation
- Window Execution Plan
- Micro-Batch Streaming
- Caching Strategy

---

## 📊 Sample Analytical Output

- Revenue per Country
- Top Customers per Country (Ranked)
- Performance benchmarking comparison

---

## ▶ How to Run

### 1️⃣ Install dependencies
pip install -r requirements.txt


### 2️⃣ Open the Notebook

Run all cells in:
spark_bigdata_analytics_pipeline.ipynb

---

## 📌 Resume Impact Statement

Designed and implemented a scalable Apache Spark Big Data analytics pipeline processing 1M+ records with window functions, structured streaming, partition optimization, and performance benchmarking.

---

## 👨‍💻 Author

MTech – Big Data Analytics  
Apache Spark Project – Portfolio Demonstration


