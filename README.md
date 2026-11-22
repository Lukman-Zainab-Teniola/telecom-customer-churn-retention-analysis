# Telecom Customer Churn & Retention Analysis

**An end-to-end Excel and Power BI portfolio case study using 5,000 synthetic telecom customer records.**

![Customer churn dashboard](assets/customer_churn_dashboard.png)

## Project at a glance

| Metric | Value |
|---|---:|
| Customers | 5,000 |
| Churned | 1,445 |
| Retained | 3,555 |
| Churn rate | 28.9% |
| Retention rate | 71.1% |

**Tools:** Microsoft Excel, Microsoft Power BI, DAX.  
**Dataset:** Synthetic, 5,000 customer-level rows and 22 fields; snapshot date 2025-12-31.  
**Scope:** Self-initiated portfolio project; not client work or real company data.

## Business problem

Customer churn can undermine recurring revenue and long-term customer relationships. This project examines which customer groups in a simulated telecommunications dataset show comparatively higher churn and how a dashboard can support retention-focused investigation.

**Guiding question:** Which customer segments exhibit higher churn rates, and what patterns merit further business investigation?

## Objectives

- Validate the customer-level dataset and document its structure.
- Measure churn, retention and customer counts.
- Compare churn across contract types, tenure groups, payment methods and internet services.
- Examine average monthly charges and senior-citizen/partner segments.
- Present the results in an interactive Power BI dashboard and translate observations into testable business recommendations.

## Data and preparation

The supplied workbook contains the `Customers`, `Data_Dictionary`, and `Dataset_Notes` worksheets. The cleaned `Customers` sheet contains 5,000 records, 22 columns, 5,000 distinct Customer IDs, and no blank cells. The data dictionary defines each field; the dataset notes identify the data as synthetic. The currency metadata describes `MonthlyCharges` and `TotalCharges` as synthetic USD values; these are not real revenues.

The project workflow describes Excel inspection and validation (duplicate IDs, blanks, column labels, data types, category consistency, unusual values, and date display), followed by Power BI analysis. The original uncleaned dataset and step-by-step transformation history are not included, so this repository does **not** claim a measured number of corrected or removed records.

## Analytical workflow

1. Inspect and validate the dataset in Excel.
2. Import the prepared data into Power BI.
3. Develop measures for customer count, churned count, retained count, churn rate and retention rate.
4. Segment tenure into 0–12, 13–24, 25–48, and 49–72 months.
5. Compare churn across customer attributes.
6. Build an interactive dashboard with contract, internet-service and payment-method slicers.
7. Interpret patterns and propose areas for further investigation.

**KPI definitions:** Churn rate = churned customers ÷ total customers; retention rate = retained customers ÷ total customers. The exact DAX source and Power BI `.pbix` file are not included in the supplied materials, so no unverified DAX code is represented as original project code.

## Dashboard

![Full Power BI dashboard](assets/customer_churn_dashboard.png)

The dashboard includes five KPI cards; churn charts for tenure, contract, payment method and internet service; average monthly charges by churn status; and a senior-citizen/partner segment matrix.

## Key findings

| Dimension | Observed result | Interpretation |
|---|---|---|
| Contract | Month-to-month: **45.6%**; one-year: 13.9%; two-year: 9.1% | Month-to-month customers have the highest observed churn rate. |
| Tenure | 0–12 months: **51.2%**; 13–24: 31.1%; 25–48: 27.5%; 49–72: 17.1% | Churn is highest in the earliest tenure group. |
| Payment | Electronic check: **36.3%**; credit card automatic: 26.7%; bank transfer automatic: 24.9%; mailed check: 23.2% | Electronic-check customers have the highest observed churn. |
| Internet | Fiber optic: **33.3%**; DSL: 26.1%; no internet: 20.5% | Fiber-optic customers have the highest observed churn. |
| Monthly charges | Churned: **98.60**; retained: **94.54** | Churned customers have higher average monthly charges (difference 4.06). |
| Senior status | Senior: **33.8%**; non-senior: 28.0% | Higher churn is observed among senior customers. |

**Visuals from the actual dashboard:**

![Churn by contract](assets/churn_by_contract.png)
![Churn by tenure](assets/churn_by_tenure.png)
![Churn by payment](assets/churn_by_payment.png)
![Churn by internet](assets/churn_by_internet.png)
![Average monthly charges](assets/monthly_charges_by_churn.png)
![Customer segment matrix](assets/customer_segment_matrix.png)

## Business recommendations to investigate

1. **Month-to-month contracts:** Explore customer expectations, pricing and possible longer-term plan incentives.
2. **First-year customers:** Review onboarding, early support and service activation experiences.
3. **Electronic-check customers:** Investigate payment convenience, billing friction and complaints.
4. **Fiber-optic customers:** Examine perceived value, service quality and reliability.
5. **Higher-charge customers:** Investigate value-for-money perceptions and service mix.
6. **Senior customer segments:** Explore support needs and segment-specific experience differences.

These are **hypotheses for investigation**, not proven causes or tested interventions.

## Limitations

- Synthetic data cannot establish real-world telecom customer behaviour.
- This is descriptive analysis, not causal inference or predictive modelling.
- Differences may reflect confounding factors not controlled for here.
- The repository contains the cleaned dataset, not an original raw-to-clean transformation log.
- No real-world retention uplift, revenue impact, or deployed solution is claimed.

## Repository contents

```text
Telecom_Churn_GitHub_Portfolio/
├── README.md
├── data/
│   └── customer_churn_cleaned.xlsx
├── assets/
│   ├── customer_churn_dashboard.png
│   └── [six cropped visuals from the original dashboard]
├── presentation/
│   └── telecom_churn_case_study.pptx
└── docs/
    └── medium_article_draft.md
```

## How to explore

1. Open `assets/customer_churn_dashboard.png` to view the finished dashboard.
2. Open `data/customer_churn_cleaned.xlsx` for the synthetic dataset, dictionary and notes.
3. Open `presentation/telecom_churn_case_study.pptx` for the presentation narrative.
4. Read `docs/medium_article_draft.md` for a longer explanation of the analysis.

**Optional next addition:** Include the original `.pbix` file and verified DAX measures, if available, to make the work reproducible in Power BI.

## Author

**Zainab Teniola Lukman**  
Data Analytics | Business Intelligence | Data Research  
[LinkedIn](https://www.linkedin.com/in/zainab-lukman/)

*This is a portfolio demonstration using synthetic data.*
