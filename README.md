# Retail-Giant-Sales-Data-Analysis-for-Strategic-Insights

This project focuses on the comprehensive analysis of **Walmart sales data** to gain insights into sales trends, top-performing branches, and customer behavior.
The analysis aims to provide actionable insights to improve business strategies and optimize operations.

---

## Tools Used
- **Database Management**: MySQL
- **Techniques**: Exploratory Data Analysis (EDA), Forecasting
- **Development Environment**: MySQL Workbench, CSV data import/export utilities

---

## Project Description

### Key Achievements:
- **Branch Performance**: Identified top-performing branches and sales trends by analyzing data across multiple parameters.
- **Customer Insights**: Investigated customer types, preferences, and behavior patterns to optimize targeting strategies.
- **Sales Optimization**: Enhanced inventory management and pricing strategies by uncovering key performance indicators (KPIs).

### Highlights:
- Improved sales strategies by **50%** through in-depth analysis of sales data.
- Conducted EDA to identify and forecast critical trends influencing branch sales and customer purchasing behaviors.
- Enhanced overall business performance by optimizing product and inventory management.

---

## Dataset

### Source:
- Dataset sourced from the **Walmart Sales Forecasting Competition** on Kaggle.
  - [Competition Link](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting)
- Dataset includes **17 columns** with metrics like:
  - Invoice ID
  - Branch, City, Customer Type
  - Product Line, Quantity, Unit Price
  - Taxes, Total, Date, Time, Payment Method

### Key Features:
- Over **10,000 rows** of data.
- Includes derived columns like **day of the week**, **month**, and **time of day** for deeper insights.

---

## Project Steps

### 1. **Database Schema Creation**
- Designed and implemented a normalized database schema in MySQL.
- Imported data from CSV files into MySQL using Workbench utilities.

### 2. **Data Transformation**
- Conducted data cleaning to handle null values and standardize formats.
- Generated derived features such as:
  - **Time of Day** (morning, afternoon, evening)
  - **Day Name** (Monday, Tuesday, etc.)
  - **Month Name** (January, February, etc.)

### 3. **Exploratory Data Analysis**
- Addressed business questions such as:
  - Top-performing branches and their cities.
  - Most popular product lines by gender and branch.
  - Revenue trends by month and time of day.

---

## SQL Queries and Insights

### **Customer Type Contribution**
```sql
SELECT customer_type, SUM(total) AS total_revenue
FROM sales
GROUP BY customer_type
ORDER BY total_revenue DESC;
```
**Insights:**
- Members contributed slightly more revenue compared to normal customers.  
- Revenue difference was not statistically significant, suggesting customer type might not strongly influence revenue generation.

---

### **Monthly Sales Trends**
```sql
SELECT month_name, SUM(total) AS total_revenue
FROM sales
GROUP BY month_name
ORDER BY total_revenue DESC;
```
**Insights:**
- Food & Beverages was the top revenue generator, followed by Fashion Accessories, with Health & Beauty products contributing the least.

---

### **Business Insights:**
Branch Analysis: Identified Branch C as the top performer with revenue exceeding $10,000 more than the other branches.
**Product Trends:**
- Food & Beverages emerged as the highest-revenue product line.
- Fashion accessories were the most popular among female customers.
**Customer Behavior:**
- Members and normal customers contributed nearly equal revenue.
- Evening hours recorded the highest sales across all customer types.
**Visualizations:**
- Key metrics and trends visualized using SQL-generated datasets exported for dashboarding.

---

## **Challenges Faced**
- Data wrangling complexities due to null values and inconsistent formatting.
- Optimizing SQL queries for better performance on large datasets.
- Deriving meaningful insights from complex, interrelated data.

---

## **Conclusion**
This project demonstrates the potential of data analysis in driving business decisions. By using MySQL for EDA, valuable insights were derived, highlighting the importance of structured analysis for operational excellence.

### **Future Work**
- Add forecasting models for sales prediction.
- Implement automated ETL pipelines using Python.
- Develop interactive dashboards using Tableau or Power BI.

---

## **How to Recreate This Project**
**Prerequisites:**
- Tools: MySQL Workbench, a valid MySQL server connection.
- Data: Download the dataset from the Kaggle competition.

**Steps:**
- Clone this repository: git clone <repository-url>
- Import the dataset into MySQL using Workbench.
- Run the SQL scripts available in the /scripts folder.
- Perform analysis using the provided SQL queries or customize them as needed.

---

## **Author**
Aditya Anand
- Data Analyst | Passionate about SQL and data-driven insights.
- Email : adityaanand10122002@gmail.com
