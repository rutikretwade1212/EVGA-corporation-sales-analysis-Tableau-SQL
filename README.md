# Sales Insights Data Analysis Project

Welcome to the **Sales Insights Data Analysis Project**! This repository demonstrates data analysis using **MySQL** and **Tableau** to gain actionable insights from sales data. The project showcases how to use SQL for querying datasets and Tableau for visualizing the results.

---

## Project Overview

This project involves analyzing sales data stored in a relational database. The dataset includes information about customers, transactions, and markets. Using SQL queries, we extract meaningful insights from the data, such as customer trends, revenue generation, and market performance. The findings are then visualized in an interactive Tableau dashboard.

---

## Key Features

1. **SQL-Based Data Analysis**  
   Perform complex queries to analyze sales trends, customer behavior, and revenue distribution.

2. **Interactive Tableau Dashboard**  
   Gain insights through a visually appealing and user-friendly dashboard.  

3. **Data-Driven Decision Making**  
   Utilize insights to improve market strategies and customer engagement.

---

SQL Queries for Analysis
Here are some key SQL queries used in the project:

1. Show all customer records:
sql
Copy code
SELECT * FROM customers;
2. Show the total number of customers:
sql
Copy code
SELECT COUNT(*) FROM customers;
3. Show transactions for the Chennai market:
sql
Copy code
SELECT * FROM transactions WHERE market_code='Mark001';
4. Show distinct product codes sold in Chennai:
sql
Copy code
SELECT DISTINCT product_code FROM transactions WHERE market_code='Mark001';
5. Show transactions where currency is in USD:
sql
Copy code
SELECT * FROM transactions WHERE currency="USD";
6. Show transactions in 2020 (using a join with the date table):
sql
Copy code
SELECT transactions.*, date.* 
FROM transactions 
INNER JOIN date 
ON transactions.order_date = date.date 
WHERE date.year = 2020;
7. Show total revenue in 2020:
sql
Copy code
SELECT SUM(transactions.sales_amount) 
FROM transactions 
INNER JOIN date 
ON transactions.order_date = date.date 
WHERE date.year = 2020 
AND (transactions.currency="INR" OR transactions.currency="USD");
8. Show total revenue in January 2020:
sql
Copy code
SELECT SUM(transactions.sales_amount) 
FROM transactions 
INNER JOIN date 
ON transactions.order_date = date.date 
WHERE date.year = 2020 
AND date.month_name = "January" 
AND (transactions.currency="INR" OR transactions.currency="USD");
9. Show total revenue in 2020 for Chennai:
sql
Copy code
SELECT SUM(transactions.sales_amount) 
FROM transactions 
INNER JOIN date 
ON transactions.order_date = date.date 
WHERE date.year = 2020 
AND transactions.market_code = "Mark001";
Tableau Dashboard
The Tableau Dashboard provides an interactive visualization of the sales insights derived from the SQL queries. It includes key metrics such as:

Total revenue by year and market
Customer distribution and trends
Product performance across regions
Dashboard Preview

Add a link to your Tableau Public profile or embed the dashboard directly.

Insights and Findings
Chennai Market Analysis

Identified key products contributing to sales.
Highlighted significant revenue generation in specific time periods.
Revenue Trends

The year 2020 showed peak revenue during January.
USD transactions contributed a substantial share of sales.
Customer Base

Total customers in the dataset and their transactions were analyzed to understand patterns and behaviors.
How to Explore the Dashboard
Download Tableau Public or open the embedded dashboard link.
Navigate through the interactive visualizations.
Use filters and controls to explore specific insights.
Conclusion
This project demonstrates the power of SQL and Tableau for data-driven decision-making. By combining analytical queries with interactive dashboards, businesses can gain a deeper understanding of their sales performance and customer trends.







