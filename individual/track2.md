# Turning a Recommendation into Reality

## What would be implemented:  
We would operationalize a lifecycle-driven retention strategy within the high-risk month-to-month population. Customers in months 1–6 would receive add-on and auto-pay promotions to build habit and reduce payment friction, while customers beyond 6 months would receive targeted contract-conversion incentives to increase commitment.

## Success Metric & Baseline:  
The primary success metric is reduction in churn rate versus a control group. The overall churn baseline in our dataset is approximately 23%, with materially higher concentration in early-tenure customers.

A critical guardrail metric is Average Revenue Per User (ARPU) to ensure that improved retention is not achieved through unsustainable margin trade-offs.

## Measuring Impact:  
We would begin with a small randomized pilot within each lifecycle band. Eligible customers would be split into treatment and control, and churn would be tracked over a 60–90 day window.

Observed uplift would be calculated as:  
**uplift = churn(control) − churn(treatment)**

If the pilot demonstrates positive economics, results would be scaled by training uplift models to prioritize customers where uplift × customer lifetime value (CLV) exceeds incentive cost, protecting profitability as campaigns expand.

### Key Risks & Unintended Consequences:  
1. **Engagement dilution** — customers may accept promotions without increasing real product usage, limiting stickiness.  
2. **Incentive conditioning** — repeated offers may encourage customers to delay decisions in expectation of future discounts, raising long-term retention costs.
