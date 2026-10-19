# Retail Sales Performance — Power BI

## Problem
Which product lines and branches drive the most profit, and are there day-of-week or time-of-day patterns strong enough to justify changing staffing or promotions?

## Data
- **Source:** "Supermarket Sales" dataset, Kaggle (search "supermarket sales" — 3 branches, ~1,000 transactions, fields include branch, city, product line, unit price, quantity, date, time, payment method, gross margin, rating)
- **Size:** ~1,000 rows × 17 columns
- **Cleaning notes:**
  - [ ] Confirm no duplicate invoice IDs
  - [ ] Split `Date` and `Time` into separate date/hour columns for time-of-day analysis
  - [ ] Check for consistent formatting in `Product line` and `City` categories
  - [ ] Create a `Day of Week` calculated column
  - [ ] Verify `gross margin percentage` is constant (it is in this dataset — worth noting, not calculating per row)

## Approach
- Tool: Power BI Desktop
- Data model: single flat table (no relationships needed — this dataset doesn't require a star schema)
- Key DAX/measures to build:
  - `Total Revenue = SUM(Sales[Total])`
  - `Total Profit = SUM(Sales[gross income])`
  - `Avg Rating = AVERAGE(Sales[Rating])`
  - `Revenue by Hour = ` time-intelligence measure using the extracted hour column
- Visuals: KPI cards (revenue, profit, avg rating) at top; bar chart of profit by product line; matrix or heatmap of sales by hour × day of week; branch comparison (clustered bar or map if you have lat/long)

## Key Insights
*(Fill these in with your actual numbers once the dashboard is built — this is where a recruiter's eyes go first)*
- Which product line contributes disproportionately to profit vs. its share of transactions?
- Is there a branch that underperforms on rating despite strong revenue — worth investigating why?
- Do sales cluster in a few hours of the day? If so, note the actual time window and what staffing change it implies.

## Dashboard
![screenshot](../assets/01-retail-sales-dashboard.png)
🔗 [Live interactive dashboard](ADD-YOUR-PUBLISH-TO-WEB-LINK-HERE)
