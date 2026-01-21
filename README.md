# TASK-3
INTERNSHIP DAY 3


Task 3: SQL Basics - Filtering, Sorting, Aggregations

This README documents the SQL queries written to complete Task 3 of the Data Analyst Internship assignment. The dataset used is sales_summary.csv, containing 20 rows of retail sales data.

# Queries Written and Their Purpose

1. Basic Preview and Verification

SELECT * FROM sales LIMIT 5;
SELECT COUNT(*) FROM sales;

Preview the first few rows and verify total records.

2. Filtering with WHERE

SELECT * FROM sales WHERE Category = 'Technology'; SELECT * FROM sales WHERE Region = 'West'; SELECT * FROM sales WHERE Discount > 0.10;

Filter rows based on category, region, and discount.

3. Sorting with ORDER BY

SELECT Product, Sales FROM sales ORDER BY Sales DESC LIMIT 5;
SELECT Product, Profit FROM sales ORDER BY Profit ASC LIMIT 5;

Identify top-selling and lowest-profit products.

4. Aggregations with GROUP BY

SELECT Region, SUM(Sales), AVG(Profit), COUNT(*) FROM sales GROUP BY Region;
SELECT Category, COUNT(*) FROM sales GROUP BY Category;

Summarize sales and profit by region and count orders by category.

5. HAVING Clause

SELECT Category, SUM(Sales) FROM sales GROUP BY Category HAVING SUM(Sales) > 100000;
SELECT Region, AVG(Profit) FROM sales GROUP BY Region HAVING AVG(Profit) > 5000;

Filter grouped results based on aggregated conditions.

6. Date Range with BETWEEN

SELECT OrderDate, SUM(Sales) FROM sales WHERE OrderDate BETWEEN '2025-02-01' AND '2025-02-28' GROUP BY OrderDate ORDER BY OrderDate;

Generate a monthly sales report for February 2025.

7. Pattern Search with LIKE

SELECT OrderID, CustomerName FROM sales WHERE CustomerName LIKE '%an%';
SELECT Product FROM sales WHERE Product LIKE '%Desk%';

Search for customer names and products matching specific patterns.

8. Top 5 Customers by Spend

SELECT CustomerName, SUM(Sales) AS TotalSpend FROM sales GROUP BY CustomerName ORDER BY TotalSpend DESC LIMIT 5;

Identify the top 5 customers based on total spending.

 Deliverables:

queries_task3.sql: Contains all SQL queries listed above.

sales_summary.csv: Dataset used for analysis.

README.md: This file explaining the queries and their purpose.

 Outcome:

Gained confidence in SQL basics: filtering, sorting, grouping, and aggregations.

Practiced real-world data analysis using SQL.
