# What 5,000 Telecom Customer Records Revealed About Churn and Retention | An Excel & Power BI Case Study

*How I used data preparation, DAX-based KPIs, customer segmentation and an interactive dashboard to investigate customer churn patterns.*

Customer churn is one of the most important measures for a subscription business. Knowing how many customers leave is useful, but understanding **which customer groups have higher churn** can make the analysis more actionable.

For this self-initiated portfolio project, I analysed **5,000 synthetic telecommunications customer records** using **Microsoft Excel, Power BI and DAX**. My goal was to move beyond a dashboard of numbers and build a structured case study: start with a business question, validate the data, develop useful measures, explore customer segments, and turn the patterns into recommendations for further investigation.

> **Data disclosure:** This dataset is simulated. The findings demonstrate an analytical approach; they are not claims about a real telecom provider.

## The business question

**Which customer segments show higher churn rates, and what should a telecommunications business investigate to improve retention?**

I focused on contract types, customer tenure, payment methods, internet service, monthly charges and demographic/relationship segments.

## Understanding and preparing the dataset

The workbook contains 5,000 customer records and 22 fields, with a data dictionary and dataset notes. In Excel, the preparation workflow covered checking duplicates, missing values, column names, data types, categorical consistency, unusual values and date formatting. The supplied cleaned workbook has 5,000 distinct Customer IDs and no blank cells.

This is an important distinction: I can describe the validation process, but without the original raw file and a transformation log, I cannot claim that a specific number of errors were corrected or rows removed.

## From data to KPIs in Power BI

I used Power BI and DAX to structure the analysis around five headline measures:

- **Total customers:** 5,000
- **Churned customers:** 1,445
- **Retained customers:** 3,555
- **Churn rate:** 28.9%
- **Retention rate:** 71.1%

The churn rate is the number of churned customers divided by total customers. I also grouped tenure into four ranges (0–12, 13–24, 25–48 and 49–72 months) to compare patterns across customer lifecycles.

## The dashboard

![My Power BI customer churn and retention dashboard](../assets/customer_churn_dashboard.png)

*Figure 1. Original Power BI dashboard, featuring KPI cards, churn comparisons and interactive slicers for contract, internet service and payment method.*

The dashboard was designed to answer both the high-level question—how much churn is present?—and the more useful follow-up: where is churn concentrated?

## Six findings that stood out

### 1. Month-to-month customers had the highest churn rate

![Churn by contract](../assets/churn_by_contract.png)

Month-to-month customers recorded **45.6% churn**, compared with **13.9%** for one-year and **9.1%** for two-year contracts. This identifies a segment worth examining, but does not prove that contract duration itself causes churn.

### 2. The earliest tenure group showed the highest churn

![Churn by tenure](../assets/churn_by_tenure.png)

Customers in their first 12 months recorded **51.2% churn**. The rates were **31.1%** for months 13–24, **27.5%** for months 25–48, and **17.1%** for months 49–72. This suggests that onboarding and early customer experiences deserve investigation.

### 3. Electronic-check customers had the highest churn

![Churn by payment method](../assets/churn_by_payment.png)

Electronic-check customers recorded **36.3% churn**, higher than the other payment groups shown in the dashboard. Payment method is an association here, not a demonstrated reason for leaving.

### 4. Fiber-optic customers had the highest churn among internet groups

![Churn by internet service](../assets/churn_by_internet.png)

The fiber-optic group recorded **33.3% churn**, compared with **26.1%** for DSL and **20.5%** for customers without internet service. This motivates follow-up questions about service quality, expectations, and perceived value.

### 5. Churned customers had higher average monthly charges

![Average monthly charges](../assets/monthly_charges_by_churn.png)

The average monthly charge was **98.60** among churned customers and **94.54** among retained customers, a difference of **4.06** in the dataset's synthetic USD units. This does not establish that higher charges caused churn.

### 6. Senior customers showed higher churn

![Senior-citizen and partner segment matrix](../assets/customer_segment_matrix.png)

Senior customers recorded **33.8% churn**, compared with **28.0%** among non-senior customers. Within the displayed senior/partner segments, senior customers with partners recorded **35.4%**. Segment differences should be interpreted carefully, particularly without additional controls.

## Translating findings into possible actions

If I were presenting these results to a retention team, I would propose six lines of investigation: review month-to-month customer experiences and plan options; evaluate first-year onboarding; examine electronic-check billing friction; assess fiber-optic service satisfaction; explore perceived value among higher-charge customers; and understand the support needs of senior customer groups.

These are **investigation priorities**, not guaranteed solutions. The next analytical step would be to test whether the patterns persist after accounting for overlapping customer characteristics, and then evaluate proposed interventions with appropriate measurement.

## What this project demonstrates

This case study allowed me to bring together **Excel data validation, Power BI, DAX KPI development, customer segmentation, data visualisation and business communication**. The most valuable part was not producing charts alone; it was deciding which comparisons mattered, explaining what they showed, and being precise about what they could not prove.

## Limitations and next steps

The dataset is synthetic, so the patterns are not evidence of actual telecom behaviour. The analysis is descriptive and does not estimate causal effects or forecast future churn. The repository contains the cleaned workbook and dashboard screenshots; the Power BI source file and exact DAX definitions can be added separately if available.

For a next iteration, I would examine segment sizes and cross-segment relationships, validate DAX calculations against the dataset, and consider predictive modelling only after defining a clear evaluation objective.

## Explore the project

**GitHub repository:** [Add your published GitHub repository URL]  
**Project presentation:** [Link to presentation in GitHub repository]  
**LinkedIn:** https://www.linkedin.com/in/zainab-lukman/

*Written by Zainab Teniola Lukman — Data Analytics | Business Intelligence | Data Research.*
