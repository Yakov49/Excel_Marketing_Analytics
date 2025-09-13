# Introduction
This project analyses multi-channel marketing performance by using Excel. Using daily sessions/clicks/spend and order-level revenue, the workbook builds pivots and KPIs to answer:

Which channels drive the most orders and revenue?
How efficient are we (CTR, CPC, CR, CAC, ROAS, AOV)?
How do results trend by week and month?

# File in this repo
`Excel.xlsx` – the complete workbook (pivots, formulas, and charts).
I keep only the workbook in the repo; charts for the README are pasted inline below.

# What’s inside the workbook
**Sheets (typical layout):**
 `sessions` – daily traffic by Channel/Source/Medium (sessions, clicks, spend, CTR, date, week, month).
 `orders` – order-level data (order date, items, revenue, channel attribution).
 `weekly_summary` – weekly rollups (spend, orders, revenue).
 `channel_summary` – pivoted channel KPIs (CR, AOV, CAC, ROAS, trend columns).
 `report / kpi_pivot` – a tidy report view that references the pivots.

**KPIs & formulas**
- **CTR** = `Clicks / Sessions`  
- **CPC** = `Adjusted Spend / Clicks`  
- **CR**  = `Orders / Sessions`  
- **AOV** = `Revenue / Orders`  
- **CAC** = `Adjusted Spend / Orders`  
- **ROAS** = `Revenue / Adjusted Spend`

> Paid channels use Adjusted Spend (to allow a CPC multiplier for scenario testing). Organic/Email/Referral have £0 spend; CAC/ROAS are N/A for those.

**Excel features used**

PivotTables & PivotCharts with slicers

Date functions (week number, month, EOMONTH)

Lookups/mappings for channel grouping

Conditional formatting for KPI thresholds

# Visuals

### Monthly trend
Sessions by month show seasonality and help spot tracking issues or partial months.

**PASTE 1ST GRAPH HERE (Sessions by month)**

_Add a one-liner once pasted, e.g.: “Sessions peaked in Jun/Jul before a sharp drop in Aug (likely seasonal or partial month data).”_

### Weekly efficiency view
Overlay spend and orders to see how budget translates into conversions week-to-week.

**PASTE 2ND GRAPH HERE (Weekly spend & orders)**

_Possible read: “Spend is fairly steady across weeks; orders fluctuate—investigate creative/landing page changes around weeks with dips.”_



# How to use the workbook
1. Open `Excel.xlsx` (Excel 2019 / O365 recommended).  
2. Go to **Data → Refresh All** to recalc pivots.  
3. Use slicers (Channel/Month/Source) to explore segments.  
4. Optional scenario: adjust the **CPC multiplier** on the report sheet to see CPC/CAC/ROAS sensitivity.



# Results & quick insights (template)
- **Best converting channel**: Email typically leads CR in most ecommerce datasets.  
- **Largest order driver**: Organic Search often leads order volume—protect SEO.  
- **Paid mix**: Compare ROAS and CAC between Paid Search vs Paid Social; shift budget toward the better unit economics.  
- **Health check**: Investigate any sudden weekly drops (partial weeks, tracking, promos).

> Replace these bullets with your actual takeaways after you review the pivots.



# Next steps
- Power Query to auto-load new CSVs each month.
- A single-page **Dashboard** (slicers + headline KPIs + small multiples).
- Cohort analysis for **repeat rate** and **LTV : CAC** by channel.
- Export key charts as PNGs for monthly reporting.



