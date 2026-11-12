# From Chaos to Clarity: Automated E-Commerce Data Engineering Pipeline

## Project Overview
Real world data is chaotic, inconsistent and manually entered. This project replicates an unmoderated data engineering problem.
I built a programmatic Python pipeline to ingest corrupt retail transactions dataset, audit its quality, handle structural flaws,
and export a business-ready dataset optimized for financial forecasting.

## Tech Stack & Skills Demonstrated
* **Languages & Tools:** Python, VS Code, Jupyter Notebooks, Git, GitHub
* **Libraries:** Pandas, NumPy
* **Core Competencies:** Data Auditing, Type Coercion, Logical Value Imputation, Outlier Handling, Automation Pipelines

## The Data Quality Ledger (Before vs. After)
This ledger highlights the critical data quality issues uncovered during programmatic discovery and the systematic strategy
implemented to resolve them.

| Data Metric / Column | Detective Work (Issues Uncovered) | Engineering Strategy (The Fix) | Strategic Business Impact |
| :--- | :--- | :--- | :--- |
| **Column Headers** | Hidden Whitespace padding (e.g., 'Order_ID'). | Applied Vector string clearing via '.columns.str.strip()'. | Previous catastrophic relational syntax errors during downstream database joins. |
| **Price Column** | Contained corrupted alphabet text strings (like 'abd'). | Used 'errors='coerce' to strip text and fill gaps using distribution-safe 'median' pricing. | Reclaims valuable sales records without skewing financial averages or throwing application crashes. |
| **Quantity Column** | Contained missing inputs ('NaN') and impossible negative values. | Purged negative transaction system anomalies; imputed missing spaces via median distribution. | Restored mathematical tracking integrity for inventory volume and logistical trends. |
| **Total Revenue** | Missing values ('Nan') across key transactions. | Constructed a deterministic logic loop calculating 'Total = Quantity x Price'. | Secures 100% mathematical precision across all accounting and financial balance sheets. |
| **Order_Date Column** | Text-based, non-standardized variations (mixed text format). | Standardized variations using 'pd.to_timedate()' and handled anomalies using '.min()' values. | Enabled seamless time-series forecasting, quarterly planning, and cohort retention charts. |
