💊 MediCare Pharmacy Analytics & Intelligence Dashboard

End-to-End Pharmacy Business Intelligence Solution using Python, PostgreSQL, SQL & Power BI

📌 Project Overview

The MediCare Pharmacy Analytics & Intelligence Dashboard is an end-to-end Business Intelligence project designed to analyze pharmacy retail operations, sales performance, inventory, prescriptions, customers, purchases, suppliers, stores, and profitability.

The solution combines Python for data generation and validation, PostgreSQL for database management and SQL analysis, and Power BI for interactive reporting and visualization.

The project contains 13 interconnected datasets with 837,764+ records and follows a structured star-schema data model suitable for real-world pharmacy analytics.

🎯 Business Objectives

The dashboard is designed to help pharmacy management:

Monitor overall sales and profitability

Analyze monthly and regional sales performance

Identify top and underperforming products

Understand customer purchasing behavior

Monitor prescription activity

Track inventory levels and expiry risks

Analyze purchasing and supplier performance

Compare pharmacy store performance

Identify profitability trends

Support data-driven business decisions

Monitor operational KPIs from a centralized dashboard

📊 Dataset Overview

The project contains 13 interconnected tables with 837,764+ total records.

#

Dataset

Type

Rows

Purpose

1

Fact_Sales

Fact

500,000

Pharmacy sales transactions

2

Fact_Inventory

Fact

100,000

Daily inventory records

3

Fact_Purchase

Fact

80,000

Supplier purchase transactions

4

Fact_Prescription

Fact

150,000

Prescription and medicine records

5

Dim_Customer

Dimension

5,000

Customer master information

6

Dim_Date

Dimension

2,191

Date and time intelligence

7

Dim_Product

Dimension

300

Medicine/product master

8

Dim_Store

Dimension

50

Pharmacy branch information

9

Dim_Employee

Dimension

120

Employee master information

10

Dim_Category

Dimension

12

Medicine category hierarchy

11

Dim_Payment

Dimension

5

Payment methods

12

Dim_Region

Dimension

6

Regional information

13

Dim_Supplier

Dimension

80

Supplier master information



Total



837,764



🗂️ Data Model

The project uses a star-schema approach.

Fact Tables

Fact_Sales

Fact_Inventory

Fact_Purchase

Fact_Prescription

Dimension Tables

Dim_Date

Dim_Product

Dim_Category

Dim_Customer

Dim_Store

Dim_Employee

Dim_Payment

Dim_Supplier

Dim_Region

Main Relationships

Dim_Date ───────────────┐
Dim_Product ────────────┤
Dim_Customer ───────────┤
Dim_Store ──────────────┤
Dim_Employee ───────────┤── Fact_Sales
Dim_Payment ────────────┘

Dim_Category ── Dim_Product
Dim_Region ──── Dim_Store

Dim_Date ─────── Fact_Inventory
Dim_Product ──── Fact_Inventory
Dim_Store ─────── Fact_Inventory

Dim_Date ─────── Fact_Purchase
Dim_Product ──── Fact_Purchase
Dim_Store ─────── Fact_Purchase
Dim_Supplier ──── Fact_Purchase

Dim_Date ─────── Fact_Prescription
Dim_Product ──── Fact_Prescription
Dim_Customer ─── Fact_Prescription

📈 Power BI Dashboard Pages

The Power BI report contains 12 analytical pages.

1. Executive Overview

Provides a high-level summary of pharmacy performance.

KPIs:

Total Sales

Gross Profit

Profit Margin %

Total Orders

Total Customers

Total Products

Inventory Value

Sales Growth %

Analysis:

Monthly Sales Trend

Sales by Region

Sales by Category

Top Products

Top Stores

2. Sales Analysis

KPIs:

Total Sales

Total Orders

Average Order Value

Units Sold

Discount Amount

Net Sales

Analysis:

Monthly Sales Trend

Sales by Region

Sales by Store

Sales by Customer Type

Top Products

Sales Distribution

3. Product Analysis

KPIs:

Total Products

Product Revenue

Product Profit

Average Product Margin

Analysis:

Top 10 Products

Bottom Products

Revenue by Category

Product Sales Trend

Product Profitability

Best/Worst Performing Products

4. Customer Analysis

KPIs:

Total Customers

Repeat Customers

New Customers

Average Customer Value

Analysis:

Customers by Gender

Customer Age Groups

Customer Type

Customer Growth

Top Customers

Customer Sales Contribution

5. Prescription Analysis

KPIs:

Total Prescriptions

Prescription Orders %

Average Medicines per Prescription

Prescription Sales

Analysis:

Prescription vs OTC

Top Prescribed Medicines

Prescription Trend

Diagnosis/Disease Analysis

Prescription Sales by Region

6. Inventory Analysis

KPIs:

Inventory Value

Available Stock

Expiring Soon

Out-of-Stock Items

Inventory Turnover

Analysis:

Inventory by Category

Inventory Trend

Top Fast-Moving Products

Slow-Moving Products

Expiring Products

Stock Status

7. Purchase Analysis

KPIs:

Total Purchase

Purchase Orders

Average Lead Time

Total Suppliers

Analysis:

Purchase Trend

Purchase by Category

Purchase by Supplier

Purchase by Store

Top Purchased Products

8. Supplier Performance

KPIs:

Total Suppliers

Average Supplier Rating

On-Time Delivery %

Average Lead Time

Analysis:

Supplier Ranking

Supplier Purchase Value

Supplier Rating

Delivery Performance

Lead Time Analysis

9. Store Performance

KPIs:

Store Sales

Store Orders

Store Customers

Average Profit Margin

Analysis:

Top 10 Stores

Sales by Region

Store Profitability

Store Comparison

Monthly Store Performance

10. Profitability Analysis

KPIs:

Gross Profit

Gross Margin %

Net Profit

Net Profit Margin

Analysis:

Profit Trend

Profit by Product

Profit by Category

Profit by Store

Profitability Comparison

11. Forecast Analysis

KPIs:

Forecast Sales

Growth Rate

Highest Sales Period

Lowest Sales Period

Analysis:

Monthly Sales Forecast

Trend Analysis

Forecast Confidence Interval

Seasonal Patterns

Future Sales Opportunities

12. Data Dictionary & KPI Definitions

Contains:

Data model overview

Table definitions

Primary keys

Foreign keys

Relationship definitions

KPI definitions

DAX measure descriptions

Business rules

Report information

🧮 Key Power BI Measures

Some of the main DAX measures used in the project include:

Total Sales =
SUM(Fact_Sales[Sales_Amount])

Gross Profit =
SUM(Fact_Sales[Gross_Profit])

Profit Margin % =
DIVIDE([Gross Profit], [Total Sales], 0)

Total Orders =
DISTINCTCOUNT(Fact_Sales[Invoice_No])

Total Customers =
DISTINCTCOUNT(Fact_Sales[Customer_ID])

Units Sold =
SUM(Fact_Sales[Quantity])

Average Order Value =
DIVIDE([Total Sales], [Total Orders], 0)

Inventory Value =
SUM(Fact_Inventory[Inventory_Value])

Available Stock =
SUM(Fact_Inventory[Closing_Stock])

Sales Growth % =
DIVIDE(
    [Total Sales] - [Previous Year Sales],
    [Previous Year Sales],
    0
)

🛠️ Technology Stack

Technology

Role

Python

Dataset generation, automation and data validation

Pandas

Data manipulation and processing

NumPy

Numerical operations and realistic data generation

Faker

Synthetic business/customer data generation

PostgreSQL

Relational database and data storage

SQL

Data cleaning, validation and business analysis

Power Query

Data transformation and preparation

Power BI

Data modeling, DAX and interactive dashboards

DAX

KPI calculations and analytical measures

GitHub

Project version control and portfolio documentation

🔄 End-to-End Workflow

Business Requirements
        ↓
Python
(Data Generation & Validation)
        ↓
CSV Datasets
        ↓
PostgreSQL
(Database & Data Storage)
        ↓
SQL
(Cleaning & Business Analysis)
        ↓
Power BI
(Data Modeling & Power Query)
        ↓
DAX
(KPIs & Measures)
        ↓
12-Page Interactive Dashboard
        ↓
Business Insights & Decision Support

🔍 Key Business Questions Answered

The solution helps answer questions such as:

What is the total pharmacy revenue?

Which products generate the highest sales?

Which products generate the highest profit?

Which stores perform best?

Which regions generate the most revenue?

What is the monthly sales growth?

Which customers contribute the most revenue?

How many customers are repeat customers?

Which medicines are approaching expiry?

Which products are out of stock?

Which products are fast-moving or slow-moving?

Which suppliers have the best performance?

What is the average supplier lead time?

What percentage of orders are prescription-based?

Which categories generate the highest profit?

What are the forecasted future sales trends?

📌 Data Quality & Business Rules

The project applies business rules such as:

Sales_ID is unique in Fact_Sales.

Dimension primary keys are unique.

Fact-table foreign keys can repeat.

Closing_Stock = Opening_Stock + Received - Sold.

Gross_Profit = Sales_Amount - Cost_Amount.

Profit Margin is calculated as Gross Profit divided by Total Sales.

Invoice_No may repeat when an invoice contains multiple product line items.

Date keys connect fact tables to Dim_Date.

Product, Store, Customer, Employee, Supplier and Payment IDs maintain referential integrity.

📊 Project Highlights

13 interconnected datasets

837,764+ total records

4 fact tables

9 dimension tables

12 Power BI report pages

40+ analytical KPIs and measures

Star-schema data model

PostgreSQL database

SQL analytical queries

Python-based data generation

Interactive Power BI dashboards

Time-intelligence analysis

Inventory and expiry analysis

Supplier and store performance analysis

Sales and profitability analysis

Forecasting

💼 Portfolio Value

This project demonstrates practical skills in:

Data Analytics

Business Intelligence

SQL

PostgreSQL

Python

Power BI

DAX

Power Query

Data Modeling

Data Cleaning

KPI Development

Dashboard Design

Business Analysis

It is designed as a portfolio case study that demonstrates an end-to-end analytics workflow, from raw data generation and database management through business analysis and interactive reporting.

📁 Suggested Repository Structure

MediCare-Pharmacy-Analytics/
│
├── README.md
│
├── Data/
│   ├── Fact_Sales.csv
│   ├── Fact_Inventory.csv
│   ├── Fact_Purchase.csv
│   ├── Fact_Prescription.csv
│   ├── Dim_Customer.csv
│   ├── Dim_Date.csv
│   ├── Dim_Product.csv
│   ├── Dim_Store.csv
│   ├── Dim_Employee.csv
│   ├── Dim_Category.csv
│   ├── Dim_Payment.csv
│   ├── Dim_Region.csv
│   └── Dim_Supplier.csv
│
├── Python/
│   ├── data_generation.py
│   └── data_validation.py
│
├── SQL/
│   ├── database_schema.sql
│   ├── data_import.sql
│   └── analytical_queries.sql
│
├── PowerBI/
│   └── MediCare_Pharmacy_Analytics.pbix
│
├── Documentation/
│   ├── Data_Dictionary.xlsx
│   ├── ER_Diagram.png
│   └── KPI_Definitions.pdf
│
└── Screenshots/
    ├── Executive_Overview.png
    ├── Sales_Analysis.png
    ├── Product_Analysis.png
    ├── Customer_Analysis.png
    ├── Prescription_Analysis.png
    ├── Inventory_Analysis.png
    ├── Purchase_Analysis.png
    ├── Supplier_Performance.png
    ├── Store_Performance.png
    ├── Profitability.png
    └── Forecast.png

🚀 Future Enhancements

Potential improvements include:

Real-time PostgreSQL connectivity

Automated data refresh

Machine-learning-based demand forecasting

Product demand prediction

Customer segmentation using Python

Inventory optimization

Automated low-stock alerts

Expiry-risk prediction

Advanced supplier scoring

Power BI deployment and scheduled refresh

👩‍💻 Project Summary

MediCare Pharmacy Analytics & Intelligence Dashboard demonstrates how pharmacy transaction and operational data can be transformed into actionable business intelligence using Python, PostgreSQL, SQL, Power Query, DAX and Power BI.

Dataset: 13 interconnected tables | 837,764+ records
Dashboard: 12 analytical pages | Pharmacy Retail & Operations Analytics
