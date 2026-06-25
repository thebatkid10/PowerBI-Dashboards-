# Insurance Data Analysis

## Overview
A claims and policy analytics dashboard built on a flat insurance dataset.  
Provides insights into premium revenue, claim settlement rates, policy types, and customer demographics.

## Data Source
**File:** `InsuranceData.csv`  
**Size:** 10,004 records × 13 columns

| Column | Description |
|--------|-------------|
| PolicyNumber | Unique policy ID |
| CustomerID | Unique customer ID |
| Gender | Male / Female |
| Age | Customer age (18 – 87) |
| PolicyType | Auto, Travel, Health, Home, Life |
| PolicyStartDate | Policy start date |
| PolicyEndDate | Policy expiry date |
| PremiumAmount | Premium paid |
| CoverageAmount | Maximum insured amount |
| ClaimNumber | Claim reference (null if no claim) |
| ClaimDate | Date claim was filed |
| ClaimAmount | Amount claimed (0 if no claim) |
| ClaimStatus | Settled / Pending / Rejected |

## Requirements
- Monitor total premiums collected and coverage exposure
- Track claim volume, claim amounts, and settlement rates
- Compare performance across policy types
- Analyse customer demographics (age group, gender)
- Identify active vs. expired policies

## Key Measures (DAX)
- Total Premium = SUM of PremiumAmount
- Total Claims = SUM of ClaimAmount
- Settlement Rate = Settled Claims ÷ Total Claims Filed
- Loss Ratio = Total Claims ÷ Total Premium
- Pending Claims = Count where ClaimStatus = "Pending"
- Policy Status = "Active" if EndDate ≥ Today, else "Expired"
- Age Group = 18–29 / 30–44 / 45–59 / 60+

## Dashboard Pages
**Page 1 — Policy & Premium Overview**
- KPI Cards: Total Policies, Total Premium, Active vs. Expired, Avg Coverage
- Policy distribution by type (Donut Chart)
- Premium by policy type (Bar Chart)
- Age group distribution (Column Chart)
- Gender split

**Page 2 — Claims Analytics**
- KPI Cards: Total Claims Filed, Total Claim Amount, Settlement Rate, Pending Count
- Claims by status — Settled / Pending / Rejected
- Claim amount by policy type
- Loss ratio by policy type
- Claims trend over time
- Top claims table

## Data Source
**Origin:** SQL Database  
**Exported As:** `InsuranceData.csv`  
**Size:** 10,004 records × 13 columns

The data was extracted from a SQL database using queries and stored as a CSV file,  
which was then loaded into Power BI via Power Query for transformation and reporting.
