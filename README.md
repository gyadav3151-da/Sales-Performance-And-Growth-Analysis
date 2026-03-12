# Sales Performance & Growth Analysis

## 📌 Project Overview
This project analyzes sales data to evaluate **busniness performance**, **identify profitability drivers** and **uncover opportunities for improvement**. Using **SQL for data preparation and analysis** and **Power BI for visualization**, the project explores trends across time, regions, product categories, and customer segments.

The goal of this analysis is to transform raw sales data into **actionable business insights** that can support strategic decision-making.

## 📊 Dataset
- **Source:** Superstore Sales Dataset
- **Key Fields:** Sales, Discount, Profit, Region, Category, Sub-Categories, Product, Order Date, Segment
- **Key dataset statistics:**
     - 9,994 transactions
     - 793 unique customers
     - Multiple product categories and regions

## 🧹 Data Cleaning
### 📑Excel
Initial Data Validation and feature preparation:
- Removed duplicate records
- Standardized column names for **SQL compatability**
- Verified numeric fields (sales, profit, quantity)
- Handled missing values 

### 🐍Python(Panda)
Additional preprocessing to ensure reliable SQL ingestion:
- Converted all date fields to **ISO 8601 format**(YYYY-MM-DD) to avoid locale dependent parsing issues in SQL Server
- Escaped Embedded double quotes in text fields (e.g., product names containing inch symbol) to produce a vaild CSV
- Preserved numeric integrity for fields such as Quantity, Sales and Profit
- Exported a **UTF-8 encoded**, **SQL-ready CSV** with consistent column ordering for bulk loading

## 🗃️ SQL Readiness 
- Data was loaded using a **stage table approach** to safely handle mixed data types
- Final tables were populated using safe type conversions to prevent load failures
- Created a Calendar table to assist grouping when building dashboard
- Resulting dataset is fully optimised for analytical quering

##  SQL Analysis Insights
- The dataset contains **9,994 transactions across 793 unique customers**, indicating a strong base of repeat customers and    highlighting the importance of **customer retention** for sustained revenue.
- The business generated **$2.3M in total sales with an overall profit margin of approximately 12%**, providing a healthy      baseline for profitability.
- **Sales demonstrate steady year-over-year growth**, accompanied by improving profit margins, suggesting expanding demand     and improving operational efficiency.
- **Technology products generate the highest profitability among all categories**, making them the key contributor to          overall profit performance.
- Certain subcategories, particularly **Tables** generate **negative profits largely due to high discounting** indicating a    need for pricing adjustment or cost review. 
- The **West region contributes the highest share of total sales and profit** making it a critical market for continued        investment and growth strategies.
- The **Consumer segment accounts for the largest share of total sales**, highlighting it as the primary customer segment.
- **Higher discount levels are strongly associated with lower profit margins**, indicating that aggressive discounting         strategies significantly impact profitability.

## 📊 Power BI Dashboard
An interactive **Power BI dashboard** was built to visualize key business metrics and enable dynamic exploration of sales performance.
The dashboard allows users to analyze trends across **time, regions, product categories, and customer segments** using interactive filters.

### Dashboard Pages
#### 1️⃣ Sales Overview
Provides a high-level summary of business performance.
- Key metrics displayed:
     - Total Sales
     - Total Profit
     - Profit Margin
     - Year-over-Year Sales Growth

- Visualizations include:
     - Sales trend over time
     - Sales by region
     - Sales by category
     - Top-performing products

📷 Dashboard Preview:

#### 2️⃣ Product Performance
Focuses on product-level profitability and performance.
- Visualizations include:
     - Sales vs Profit scatter analysis
     - Sales and profit by sub-category
     - Top 10 most profitable products
     - Bottom 10 least profitable products

📷 Dashboard Preview:

#### 3️⃣ Customer Analysis
Analyzes customer purchasing behavior and segment performance.

- Visualizations include:
     - Sales by customer segment
     - Customer contribution to total revenue
     - Segment-level profitability analysis
     - Distribution of sales across customer groups

📷 Dashboard Preview

#### Interactive Features
The dashboard supports filtering by:
- Year
- Region
- Category
- Customer Segment

This allows users to dynamically explore performance across different dimensions of the business.
## 🛠 Tools Used
- **Excel** - initial cleaning
- **Python(Pandas)** - data transformation and CSV preparation
- **SQL Server** - data storage and analysis
- **Power BI** - dashboard development and data visualization
