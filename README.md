# Sales Performance & Growth Analysis

## 📌 Project Overview
This project analyzes sales data to uncover trends, identify top-performing products and regions, and provide insights to support business decisions.

## 📊 Dataset
- Source: Superstore Sales Dataset
- Data includes sales, discount, profit, region, category, and order dates

## 🧹 Data Cleaning
### 📑Excel
- Removed duplicate records
- Standardized date formats
- Verified numeric fields
- Handled missing values
- Created derived features (year, month, cost, profit margin)
- Renamed columns for SQL compatibility

### 🐍Python(Panda)
- Converted all date fields to ISO 8601 format(YYYY-MM-DD) to avoid locale dependent parsing issues
- Escaped Embedded double quotes in text fields (e.g., Product_Name containing inch symbol) to produce a vaild CSV
- Enforced integer typing for numeric fields such as Quantity
- Exported a UTF-8 encoded, SQL-ready CSV with consistent column ordering

## 🛠 Tools Used
- Excel
- Python (Panda)
