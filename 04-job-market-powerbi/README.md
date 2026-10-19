# Data Analyst Job Market — Power BI

## Problem
Which skills are most requested in data analyst job postings, and how does demand vary by region and seniority level? (This one doubles as genuinely useful research for your own job search.)

## Data
- **Source:** "LinkedIn Data Analyst Jobs" dataset, Kaggle (search "LinkedIn data analyst jobs" — thousands of postings with title, location, seniority, and description/skills text)
- **Size:** Several thousand rows — check the specific file for exact column list, since these scraped datasets vary
- **Cleaning notes:**
  - [ ] Parse the job description/requirements text for skill keywords (SQL, Python, Excel, Tableau, Power BI, R, etc.) — this is the main cleaning task, likely done in Power Query with a set of "contains" flags per skill
  - [ ] Standardize location fields (city/state/country formatting is often inconsistent in scraped data)
  - [ ] Bucket seniority into consistent tiers (Entry / Mid / Senior) if the raw field is messy
  - [ ] Remove duplicate postings if the same job appears multiple times

## Approach
- Tool: Power BI Desktop
- Data model: single table, with calculated columns/measures flagging skill mentions
- Key measures:
  - `Postings Mentioning SQL = COUNTROWS(FILTER(Jobs, Jobs[Contains SQL] = TRUE))`
  - Repeat pattern for each skill you're tracking
  - `% of Postings = DIVIDE([Postings Mentioning Skill], [Total Postings])`
- Visuals: horizontal bar chart of skill frequency (ranked), map or bar chart of postings by region, matrix of skill frequency by seniority level, slicer for region/seniority

## Key Insights
*(Fill these in once you've run the actual skill-frequency counts)*
- Which 3 skills appear in the highest share of postings — does this match or differ from what you expected?
- Does skill demand shift noticeably between entry-level and senior postings (e.g., more Python/statistics at senior level)?
- Is there a regional skill difference worth noting (e.g., one tool more dominant in one market)?

## Dashboard
![screenshot](../assets/04-job-market-dashboard.png)
🔗 [Live interactive dashboard](ADD-YOUR-PUBLISH-TO-WEB-LINK-HERE)
