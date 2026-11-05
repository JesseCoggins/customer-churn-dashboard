# A technical walkthrough of telecom churn

[Open the live Tableau dashboard](https://public.tableau.com/app/profile/jesse.coggins6637/viz/ChurnRateDashboard_17756852469330/CustomerChurnDashboardKeyTrendsbyIncomeRegionContractPayment) to follow the analysis.

## 1. Set the baseline

Start with every state and contract type selected. Of the 10,000 customers in the source, 2,650 churned. That gives an overall churn rate of 26.50%. Average monthly charge is $172.62. Both figures provide a reference when a filter changes the population on screen.

## 2. Compare contracts

Hover over the contract bars. Month-to-month customers have the highest observed churn rate in this dataset. The denominator is the number of customers on that particular contract.

| Contract | Churned | Customers | Within-contract churn |
|---|---:|---:|---:|
| Month-to-month | 2,034 | 5,456 | 37.28% |
| One year | 307 | 2,102 | 14.61% |
| Two year | 309 | 2,442 | 12.65% |

This comparison suggests a cohort for a retention experiment. It cannot establish the effect of changing a customer's contract.

## 3. Filter to a state

Select Texas on the map. Watch the headline KPIs and contract bars update together. Record the selected geography before comparing rates. The map colors show each state’s share of churned customers, rather than the within-state churn rate. Texas contributes 173 of 2,650 churners (6.53%); 173 of its 603 customers churned (28.69%). Clear the map selection to return to the national baseline.

## 4. Check the denominator for payment methods

Electronic checks account for 963 of the 2,650 churned customers, or 36.34%. Among all 3,398 electronic-check customers, the churn rate is 28.34%. For retention planning, the first percentage answers where churned customers are concentrated. The second answers how often customers in that payment group churned.

The dashboard uses numeric labels so viewers can read values alongside color. The [packaged workbook](../tableau/customer_churn_dashboard.twbx) and [source data](../data/telecom_churn.csv) accompany the walkthrough.

## 5. Interpret the income distribution

The stacked income bars show how customers are distributed across income bins and churn status. Compare a bin’s churned count with its total count before interpreting a within-bin risk. A larger orange segment by itself does not establish a higher churn probability.
