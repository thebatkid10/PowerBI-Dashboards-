
# Sales Data Analysis

## Overview
An interactive sales dashboard for ElectroHub, a retail electronics business.  
Tracks revenue, units sold, discounts, and promotional performance across products and customers.

## Data Source
**File:** `Store_Data.xlsx`

| Table | Rows | Description |
|-------|------|-------------|
| Fact Sales (Sheet3) | 3,510 | Transactions — dates, units, sales, discounts |
| Dim Customers | 50 | Customer name, city, state, contact |
| Dim Product | 30 | Product name, product line, price (INR) |
| Dim Promotion | 5 | Campaign name, ad type, coupon, discount type |

## Requirements
- Track total revenue, units sold, and average order value
- Analyse discount impact on net sales
- Measure promotional campaign effectiveness
- Identify top customers and best-performing products
- Visualise sales trends over time

## Key Measures (DAX)
- Total Revenue = SUM of Net Sales
- Net Sales = Total Sales − Discount Value
- Discount Value = Total Sales × Discount %
- Average Order Value = Total Revenue ÷ Number of Transactions
- Promotion Sales = Revenue filtered by active promotion

## Dashboard Pages
**Page 1 — Sales Overview**
- KPI Cards: Revenue, Units Sold, Avg Order Value, Total Discount
- Sales trend by month/year
- Revenue by product line
- Top 10 customers by revenue
- Sales by city/state (Map)

**Page 2 — Promotion & Discount Analysis**
- Revenue with vs. without promotions
- Discount vs. Net Sales scatter chart
- Promotion performance comparison table
- Month-on-Month / Year-on-Year revenue change

## Data Model
Star Schema — one fact table linked to three dimension tables via CustomerID, ProductID, and PromotionID.

## Tools Used
- Power BI Desktop
- Power Query (M)
- DAX
- Excel (.xlsx)
