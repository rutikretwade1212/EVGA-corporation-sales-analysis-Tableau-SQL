# Sales Insights Data Analysis Project for EVGA Corporation

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

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


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







