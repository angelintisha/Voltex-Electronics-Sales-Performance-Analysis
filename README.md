# Voltex Electronics — Sales Performance Analysis

> Analyzed 108,127 global e-commerce orders across 2019–2022 for Voltex Electronics, 
> identifying $24M in total revenue trends, product performance drivers, and 
> actionable marketing and inventory recommendations.

## Overview
An end-to-end sales analysis covering data cleaning, exploratory analysis, and 
interactive visualization for a global electronics retailer. The analysis examines 
revenue trends across products, regions, and marketing channels to surface strategic 
insights for finance, product, and marketing teams.

## Tech Stack
![Excel](https://img.shields.io/badge/Microsoft-Excel-217346?logo=microsoft-excel&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?logo=tableau&logoColor=white)

## Data Structure
Two tables were used in this analysis:

**ORDERS** — 108,127 raw rows → 92,931 clean rows · 17 columns

| Column | Description |
|--------|-------------|
| USER_ID, ORDER_ID | Customer and order identifiers |
| PURCHASE_TS / SHIP_TS / DELIVERY_TS / REFUND_TS | Order lifecycle timestamps |
| PRODUCT_NAME / PRODUCT_ID | Product details |
| USD_PRICE / LOCAL_PRICE / CURRENCY | Revenue fields |
| PURCHASE_PLATFORM | Website or mobile app |
| MARKETING_CHANNEL | Direct, email, social media, affiliate |
| ACCOUNT_CREATION_METHOD | Desktop, mobile, tablet |
| COUNTRY_CODE / LOYALTY_PROGRAM | Geographic and loyalty data |

**COUNTRY** — country-to-region mapping (NA, EMEA, APAC, LATAM)

## Data Cleaning Summary
15 issue types identified and resolved before analysis.

| Issue | Rows Impacted | Resolution |
|-------|--------------|------------|
| Duplicate rows | 15,196 | Removed; 92,931 unique rows retained |
| Missing marketing channel | 1,387 | Recategorized to "unknown" |
| Inconsistent product names | 197 | Standardized to correct spelling |
| Missing/zero USD price | 191 | Left as-is; flagged for stakeholder review |
| Inconsistent date formats | 27 | Reformatted using DATE function |
| Missing/nonsensical region values | 19 | Mapped using lookup |

## Executive Summary
- **$24.05M** in total revenue across 2019–2022 · monthly range: $166K – $883K
- **27in 4K gaming monitor** is the top product at **$8.43M** (35% of revenue)
- Sales nearly **tripled in mid-2020** driven by COVID-era demand for home electronics
- Revenue began declining in early 2021, returning toward pre-COVID levels by 2022
- **Direct channel** dominates all other marketing channels by a significant margin

## Insights Deep Dive

**Product Performance**
- Top 3 products — 27in 4K gaming monitor, Apple Airpods Headphones, Macbook Air Laptop — drive the majority of revenue and exhibit the same post-COVID plateau pattern
- Mobile (Apple iPhone) and accessories (Samsung Charging Cable Pack, Samsung Webcam) account for less than 4% of total revenue

**Regional Trends**
- All regions show similar dips in 2021–2022, confirming a global/macro trend rather than a regional issue
- Macbook Air Laptop decline is concentrated in the NA region and direct traffic channel

**Marketing Channel**
- Direct is the dominant channel across all products
- Email shows potential for growth; social media and affiliate channels remain small

## Recommendations

| Team | Recommendation |
|------|---------------|
| Product | Reassess iPhone and accessories inventory — less than 4% of revenue |
| Marketing | Invest in email channel strategy to reduce over-reliance on direct traffic |
| Marketing | Push promotions in April/May to capitalize on the consistent summer sales spike |
| Marketing | Focus NA campaigns on 27in 4K gaming monitor and Macbook Air Laptop |
| Finance | Investigate drivers of the post-COVID sales decline by product and region |
| Data | Audit marketing channel attribution — direct channel appears oversized |

## Dashboard
[![Dashboard Preview](https://public.tableau.com/static/images/Sa/SalesPerformanceDashboardProduct/Dashboard1/1.png)](https://public.tableau.com/views/SalesPerformanceDashboardProduct/Dashboard1)

**[View Interactive Tableau Dashboard →](https://public.tableau.com/views/SalesPerformanceDashboardProduct/Dashboard1)**

## Files
| File | Description |
|------|-------------|
| `Voltex_Pivot_Tables.xlsx` | Revenue pivot tables by product, month, and region |
| `Voltex_Issue_Log.xlsx` | Data quality issues identified and resolutions applied |
| `Voltex_Insights_Log.xlsx` | EDA findings, deep dive insights, and recommendations |
