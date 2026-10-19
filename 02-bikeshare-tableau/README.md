# Bike Share Ridership — Tableau

## Problem
Which stations are consistently over- or under-utilized, and how does ridership shift with season/weather? The goal is a set of findings that would inform where the operator should rebalance bikes and where new docks might pay off.

## Data
- **Source:** Citi Bike NYC system data (citibikenyc.com/system-data) — download one or two monthly trip-history CSVs to start, rather than a full year, to keep the file manageable. NYC Open Data also mirrors station-level data if you want to cross-reference.
- **Size:** Varies by month — typically several hundred thousand rows per month, so start with 1–2 months
- **Cleaning notes:**
  - [ ] Drop trips with missing start/end station data
  - [ ] Convert trip duration to minutes and flag unrealistic outliers (e.g., >6 hrs, likely a docking error)
  - [ ] Extract day-of-week and hour from `started_at`
  - [ ] If joining weather data, align on date and confirm timezone consistency

## Approach
- Tool: Tableau Public
- Worksheets to build:
  1. Map view — station locations sized/colored by trip volume (start or end counts)
  2. Line chart — daily ride count over the selected period
  3. Heatmap — rides by hour × day of week (weekday commute pattern vs. weekend leisure pattern)
  4. Optional: bar chart of top 10 busiest start stations vs. top 10 least busy
- Combine into one dashboard with a date range filter so a viewer can explore different windows

## Key Insights
*(Fill these in once you've explored the actual data)*
- Which stations show the clearest imbalance between trip starts and trip ends (a sign bikes accumulate there and need rebalancing)?
- Is there a clear commute pattern (two peaks on weekdays) vs. a flatter weekend pattern?
- Does ridership drop off sharply below a certain temperature, if you bring in weather data?

## Dashboard
![screenshot](../assets/02-bikeshare-dashboard.png)
🔗 [Live interactive dashboard](ADD-YOUR-TABLEAU-PUBLIC-LINK-HERE)
