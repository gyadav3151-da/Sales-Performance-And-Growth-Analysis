# Sales Performance & Growth Analysis

## 📌 Project Overview
This project analyzes sales data to identify **sales trends**, **top-performing products** and **high-impact regions**, providing insights to support data-driven business decisions.
This project demonstrates an end-to-end workflow from **data cleaning** to **SQL ready analytical preparations**.

## 📊 Dataset
- **Source:** Superstore Sales Dataset
- **Key Fields:** Sales, Discount, Profit, Region, Category, Product, Order Date, Ship Date

## 🧹 Data Cleaning
### 📑Excel
Initial Data Validation and feature preparation:
- Removed duplicate records
- Standardized column names for SQL compatability
- Verified numeric fields (sales, profit, quantity)
- Handled missing values
- Created derived fields
     - Year
     - Month
     - Cost
     - Profit Margin  

### 🐍Python(Panda)
Additional preprocessing to ensure reliable SQL ingestion:
- Converted all date fields to **ISO 8601 format**(YYYY-MM-DD) to avoid locale dependent parsing issues in SQL Server
- Escaped Embedded double quotes in text fields (e.g., product names containing inch symbol) to produce a vaild CSV
- Preserved numeric integrity for fields such as Quantity, Sales and Profit
- Exported a **UTF-8 encoded**, **SQL-ready CSV** with consistent column ordering for bulk loading

## 🗃️ SQL Readiness 
- Data was loaded using a **stage table approach** to safely handle mixed data types
- Final tables were populated using safe type conversions to prevent load failures
- Resulting dataset is fully optimised for analytical quering

## 🛠 Tools Used
- **Excel** - initial cleaning and feature engineering
- **Python(Pandas)** - data transformation and CSV preparation
- **SQL Server** - data storage and analysis

## 📈 Analysis Focus
The clean dataset enables analysis such as:
- Sales and profit trends over time
- Regional and Category performance
- Product-level contriution to revenue
- Discount impact on profitability 
