# Homework 3 — Survival Analysis & CLV

>Telecom subscriber churn analysis using parametric Accelerated Failure Time (AFT) models, with Customer Lifetime Value estimation and retention budget recommendations.

## Dataset
1,000 telecom subscribers with 15 features including demographics, service subscriptions, tenure, and churn status.

## Approach
1. **Kaplan-Meier** baseline survival curve
2. **Parametric AFT models** — Weibull, Log-Normal, Log-Logistic, fitted and compared via AIC, BIC, and concordance index
3. **Feature selection** — retained only statistically significant covariates (p < 0.05)
4. **CLV calculation** — discounted expected margin over a 72-month horizon per subscriber
5. **Retention budget** — identified at-risk subscribers using conditional 12-month churn probability and allocated 10% of their CLV

## Key Results
- **Best model:** Log-Normal AFT (lowest AIC = 2955.75, C-index = 0.78)
- **Significant churn drivers:** internet service, voice service, marital status, customer category, age, address tenure
- **Mean CLV:** $817 | **Median CLV:** $848
- **Annual retention budget:** ~$156 (only 6 subscribers exceed the 50% conditional churn threshold)

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook Survival_Analysis_HW_AH.ipynb
```

## Author
Albert Hakobyan