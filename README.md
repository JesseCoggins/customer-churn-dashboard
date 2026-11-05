# Telecom customer churn dashboard

**Which customers should a retention team reach first?** I built a Tableau dashboard for a telecom leadership team to compare churn across contracts, income levels, states and payment methods. Of 10,000 customers, 2,650 churned. The clearest starting point for a retention experiment was the month-to-month group.

[Open the interactive dashboard](https://public.tableau.com/app/profile/jesse.coggins6637/viz/ChurnRateDashboard_17756852469330/CustomerChurnDashboardKeyTrendsbyIncomeRegionContractPayment) · [Follow the technical walkthrough](docs/technical-walkthrough.md) · [Download the Tableau workbook](tableau/customer_churn_dashboard.twbx)

![Tableau dashboard with churn and monthly-charge KPIs above income, contract, state and payment-method views](assets/dashboard_full.png)

## What the retention team can learn

| Contract | Customers who churned | Customers on contract | Churn rate |
|---|---:|---:|---:|
| Month-to-month | 2,034 | 5,456 | 37.28% |
| One year | 307 | 2,102 | 14.61% |
| Two year | 309 | 2,442 | 12.65% |

These rates use the customers on each contract as the denominator. A retention manager could test an offer with month-to-month customers and use a holdout group to measure whether it changes churn. The dashboard alone cannot tell whether switching contracts would keep a customer.

## Inspect the workbook

Start with all states and contracts selected. Overall churn is **26.50%** and the average monthly charge is **$172.62**. Select a state on the map and watch the KPIs and contract view update together. Numeric labels help readers follow the values alongside color.

The walkthrough also explains a common source of confusion. Electronic-check users account for 36.34% of all customers who churned, while 28.34% of electronic-check users churned. Those percentages answer different questions. [Source data](data/telecom_churn.csv) · [Contract rates](assets/contract_type_churn.png) · [State share](assets/state_churn_map.png) · [Payment share](assets/payment-churn-share.png)

## Reading the measures

Payment labels and pie slices use the same churned-customer denominator. Electronic checks account for 963 of 2,650 churners (36.34%). The state map is titled **Share of Churned Customers by State**: Texas contributes 173 of 2,650 churners (6.53%), while its within-state churn rate is 173 of 603 (28.69%). Texas has the largest number of churners, not the highest within-state rate.

The income view is titled **Customer Distribution by Income**. It shows customer counts as shares of the selected population, separated by churn status. It does not establish that low-income customers have a higher churn probability. Contract bars show within-contract churn rates. The workbook is published on Tableau Public and included here with matching screenshots.

*Coursework for the M.S. in Data Analytics at Western Governors University (WGU), D601 Data Storytelling.*
