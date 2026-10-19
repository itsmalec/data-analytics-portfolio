# Global Happiness & Well-Being Trends — Tableau

## Problem
Which factors (GDP per capita, social support, healthy life expectancy, freedom, generosity, perceived corruption) correlate most strongly with a country's happiness score, and how have rankings shifted over the last decade?

## Data
- **Source:** World Happiness Report (worldhappiness.report — free CSV/Excel download each year) or the equivalent, longer-run dataset on Our World in Data
- **Size:** ~150 countries × 1 row per year — small enough to combine several years into one file
- **Cleaning notes:**
  - [ ] Standardize country names across years (report naming can shift slightly year to year — this is a common real-world data-integration snag worth documenting)
  - [ ] Confirm each year's file uses the same column definitions before appending (methodology has changed slightly across report years — note this explicitly in your README as a limitation)
  - [ ] Handle countries with missing data in some years rather than silently dropping them

## Approach
- Tool: Tableau Public
- Worksheets to build:
  1. Choropleth map — happiness score by country, with a year filter/parameter
  2. Scatter plot — GDP per capita (x) vs. happiness score (y), sized by population or colored by region, to visually assess correlation
  3. Line chart — top 5 and bottom 5 countries' happiness score trend over the last decade
  4. Optional: bar chart ranking the six sub-factors' average contribution to score
- Combine into a dashboard with a year parameter/filter so the map and scatter plot update together

## Key Insights
*(Fill these in after you calculate the actual correlations in Tableau)*
- Which single factor has the strongest visual/statistical relationship with happiness score — is it GDP, or something like social support?
- Which country moved the most (up or down) in ranking over the period you chose, and is there a plausible explanation worth a sentence?
- Are there regions where GDP is high but happiness lags the trend line — an interesting deviation worth calling out?

## Dashboard
![screenshot](../assets/03-happiness-dashboard.png)
🔗 [Live interactive dashboard](ADD-YOUR-TABLEAU-PUBLIC-LINK-HERE)
