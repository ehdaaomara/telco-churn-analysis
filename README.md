# Telecom Customer Churn Analysis

An end-to-end analysis of why customers leave a telecom company, and what the business can do to keep them. Built with Python, pandas, and seaborn.

## Project Overview

This project analyzes **7,043 telecom customers** to investigate an overall **churn rate of 26.5%** — identifying *who* is leaving, *why*, and *what actions* could reduce it. The goal was not just to describe the data, but to translate findings into concrete retention recommendations a business could act on.

## Business Question

> Which customers are most likely to leave, what drives that churn, and where should the company focus its retention efforts?

## Dataset

- **Source:** Telco Customer Churn dataset
- **Size:** 7,043 customers, 21 features
- **Features include:** demographics, account tenure, contract type, services subscribed (internet, security, support, streaming), billing, payment method, and churn status.

## Tools & Skills Demonstrated

- **Python** (pandas) for data manipulation
- **Data cleaning**: resolving data-type issues and handling missing values
- **Exploratory Data Analysis** with segmentation by customer attributes
- **Data visualization** with seaborn / matplotlib
- **Business insight**: translating findings into actionable recommendations

## Data Cleaning Notes

The `TotalCharges` column was stored as text rather than numeric because 11 records contained blank values. On inspection, all 11 had a tenure of 0 — they were brand-new customers who had not yet been billed. These values were set to 0, and the column was converted to a numeric type.

## Key Findings

| Factor | Insight |
|---|---|
| **Contract type** | Month-to-month customers churn at **42.7%** vs **2.8%** for two-year contracts — the single strongest driver. |
| **Tenure** | First-year churn is **47.7%**, falling to **9.5%** by years 4–6. The first year is the danger zone. |
| **Internet service** | Fiber optic customers churn most (**41.9%**) despite paying the most (~$91.50/mo) — the highest-value customers are the most at-risk. |
| **Payment method** | Electronic-check users churn at **45.3%** vs ~15% for automatic payments (a proxy for commitment, not a cause). |
| **Add-on services** | Customers without Online Security churn at **41.8%** vs **14.6%** with it; support and protection add-ons show the same pattern. |

## Recommendations

1. **Convert month-to-month customers to longer contracts** through targeted incentives — the cheapest, highest-impact lever.
2. **Strengthen first-year onboarding** with proactive engagement, since most churn happens early.
3. **Protect high-value fiber customers** by auditing service quality and offering loyalty pricing — they generate the most revenue and leave the most.
4. **Encourage automatic payment methods** to increase customer inertia.
5. **Bundle security and support add-ons**, especially for new and fiber customers, to raise switching costs.

## How to Run

1. Clone this repository.
2. Create a virtual environment and install dependencies:
   - pandas, matplotlib, seaborn, jupyter
3. Open `churn_analysis.ipynb` and run the cells top to bottom.

## Possible Extensions

- Build a predictive model (logistic regression / random forest) to flag at-risk customers.
- Reproduce the analysis in SQL to demonstrate database skills.
- Estimate the revenue impact of each recommendation.
