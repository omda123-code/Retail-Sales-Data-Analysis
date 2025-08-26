# Retail Sales Analysis — Business Insights with RFM (pandas/numpy/matplotlib)

## Overview
This project analyzes B2B retail sales to answer key business questions:
- Which customers are most valuable (RFM)?
- What are the time trends (month/quarter/weekday)?
- Which products and customers follow the Pareto (80/20) pattern?
- What operational issues appear in order status?

All work is done using **pandas, numpy, matplotlib** only.  
Dataset size: **2,823 rows × 25 columns**.

## Key Results
- **Top Customers (RFM)**: High `RFM_Score` customers like *Saveley & Henriot, Co.* and *Land of Toys Inc.* should be prioritized for loyalty and upsell.
- **Pareto (80/20)**: A small share of customers/products drives most revenue → focus marketing and inventory here.
- **Seasonality & Time Trends**: Clear monthly/weekday patterns to align promotions and staffing.
- **Operational**: Status analysis highlights cancellations/backorders to reduce friction.

## Figures
### Monthly Revenue
![Monthly Revenue](fig-monthly-revenue.png)

### Pareto Curve – Customers
![Pareto Curve – Customers](fig-pareto-customers.png)

### Cohort Retention
![Cohort Retention](fig-cohort-retention.png)
## Outputs
- `outputs/monthly_revenue.csv` — revenue by month/year
- `outputs/productline_revenue.csv` — revenue by product line
- `outputs/rfm_table.csv` — customer-level Recency/Frequency/Monetary and RFM_Score
- `outputs/top_customers.csv` — top customers by RFM_Score and revenue
- `outputs/cancellations_by_status.csv` — operational summary

## Notes on Method
- **RFM** via quantile-based scoring (with ties handled); when quantile edges repeat, we map categories safely and compute a stable `RFM_Score`.
- **Only** pandas/numpy/matplotlib are used (no ML).  
- Reproducible and small data footprint.

## License
MIT — feel free to use and adapt (see LICENSE).
