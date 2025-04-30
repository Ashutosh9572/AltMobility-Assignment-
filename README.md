#SQL Analysis for Alt Mobility - Order, Sales, and Payment Insights

Project Objective:-

-- The objective of this project is to analyze customer orders and payment transactions for Alt Mobility using SQL. This includes generating insights on sales trends, customer behavior, and payment statuses.


My Approach :-


1.) Initial Data Challenges :-

-> The provided datasets were in .xlsx format which is not directly usable in most SQL environments.

-> I first converted these files into .csv format so they could be imported into PostgreSQL.

-> During the import process, I encountered issues with column data types—especially the order_date, which had an incompatible format for SQL operations.


2.) Data Cleaning

-> Checked for null values and missing data to ensure query accuracy.

-> Standardized and reformatted the order_date column using SQL-compatible formats (YYYY-MM-DD) so that date-based aggregations (monthly/yearly trends) could be applied.

-> Ensured appropriate data types for all columns:

i.) order_amount and payment_amount as NUMERIC(10,2)

ii.) order_date and payment_date as DATE

iii.) Text fields as VARCHAR


3.) Loading into SQL

-> Created two tables: customers_orders and payments.

-> Loaded the cleaned CSV data into PostgreSQL using appropriate column definitions.


4.) Table Relationships

-> Both tables were joined using the common key: order_id.

-> A LEFT JOIN was used to ensure that all orders are included even if payment information is missing.


5.) SQL Analysis & Insights Extraction(Mentioned In Insights PDF)

-> Performed a range of analyses:

i.) Order and Sales Analysis: Trends by order status, total revenue, and monthly sales.

ii.) Customer Analysis: Repeat vs. one-time customers, top spenders, and ordering patterns over time.

iii.) Payment Analysis: Success vs. failure rates, payment method breakdown.

iv.) Comprehensive Order Report: Combined order and payment data to highlight issues such as failed or pending transactions.

