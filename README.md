# Walmart-Sales

🚀 Transforming Raw Sales Data into Business Intelligence

How do customer purchase behaviors and product line performance impact overall revenue? I built an end-to-end analytics workflow combining Advanced SQL and Power BI on Walmart’s transaction dataset to answer this.   🛠️ Key Technical Steps Executed:Database Engineering & Cleaning: Structured custom schemas, imported 1,000+ transactional records using LOAD DATA LOCAL INFILE, handled whitespace/nulls, and transformed raw dates/times into discrete features (time_of_day, day_name, month_name).   SQL Analytics Engine:Pareto (80/20) Analysis: Identified high-revenue products driving 80% of total revenue using running sums.   MoM Growth Tracking: Calculated sales growth rate across months using LAG() window functions.   Branch & Category Segmentation: Evaluated branch productivity and product line profitability.   Dashboard & Visualizations: Developed an executive dashboard displaying key metrics: $889.20K Sales, $42.34K Profit, 10,066 Items Sold, state-wise breakdown, and top-performing regional branches.   Check out the full SQL queries and dashboard layout in my GitHub repository! 👇🔗 [Insert Link]GitHub Repository README (README.md)Markdown# 🛒 Walmart Sales Analysis & Performance Dashboard

An end-to-end data analytics project involving database creation, data cleaning, feature engineering, advanced SQL querying, and interactive Power BI visualization on Walmart transaction data.

---

## 📌 Project Overview
This project analyzes retail transaction records to extract insights regarding sales performance, branch profitability, customer purchasing behaviors, and product-line popularity.

- **Total Sales Revenue:** $889.20K
- **Total Profit:** $42.34K
- **Total Orders Processed:** 1,000
- **Total Quantity Sold:** 10,066 units

---

## 🛠️ Tech Stack & Tools
- **Database Management:** MySQL Workbench
- **Data Querying & Analytics:** MySQL (Window Functions, CTEs, Aggregations, Data Cleaning)
- **Data Visualization:** Power BI (KPI Cards, Regional Maps, Trend Analysis Charts)
- **Data Source:** `WalmartSalesData.csv`

---

## 📑 Key Analysis & Features

### 1. Data Cleaning & Feature Engineering
- **Database Design:** Created optimized tables with proper data types (`DECIMAL`, `DATETIME`, `FLOAT`, `VARCHAR`) and primary key constraints.
- **Data Validation:** Identified and handled NULL values, empty string variations, whitespace issues, and non-positive quantity entries.
- **Time/Date Extraction:** Extracted `time_of_day` (Morning, Afternoon, Evening), `day_name`, and `month_name` columns for time-series aggregation.

### 2. Advanced SQL Analysis
- **Pareto 80/20 Rule Analysis:** Computed cumulative sales percentages using CTEs and running totals to filter products contributing to 80% of total revenue.
- **Month-over-Month (MoM) Growth:** Utilized the `LAG()` window function to calculate month-on-month sales fluctuations and growth rates.
- **Branch & Product Rankings:** Implemented `RANK()` and `DENSE_RANK()` partitioned by branches and states to identify top sales drivers.
- **Customer & Payment Insights:** Evaluated payment methods (`Ewallet`, `Cash`, `Credit Card`) and customer type profitability.

---

## 📊 Dashboard Visualizations (Power BI)
The Power BI dashboard provides executive summaries across four primary views:
1. **KPI Header Cards:** Quick view of Total Revenue ($889.20K), Total Profit ($42.34K), Order Counts (1,000), and Units Sold (10,066).
2. **Monthly Sales Trend:** Line visual highlighting peak sales months (October peak at $143.71K).
3. **Regional Heatmaps:** Geographical map visualizing high-performing regions (e.g., Maharashtra with $385K, Karnataka with $176K).
4. **Product & Branch Rankings:** Top 7 revenue-generating products (USB Flash Drives, Power Banks, Handbags) alongside top-performing store branches.
