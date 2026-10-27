# Telecom Customer Churn Prediction and Retention Analytics

## Project Overview

This project analyzes customer churn using the public IBM Telco Customer Churn dataset. It combines data cleaning, SQL, exploratory data analysis, statistical testing, machine learning, and customer risk segmentation to develop actionable retention recommendations.

## Business Problem

Customer churn can affect recurring revenue and customer relationships. The objective is to identify patterns associated with churn, predict customer churn risk, and help retention teams prioritize follow-up.

## Tools and Technologies

- Python
- Pandas and NumPy
- SQL and SQLite
- Matplotlib
- SciPy
- Scikit-learn
- Google Colab

## Dataset

The project uses the IBM Telco Customer Churn dataset, which contains customer demographics, services, contracts, charges, tenure, and churn status.

The cleaned dataset contains **7,032 records** after data cleaning.

Dataset source: [IBM Telco Customer Churn on Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn).

## Methodology

1. Cleaned and validated customer data.
2. Used SQLite and SQL to summarize customer information.
3. Explored churn patterns across contract types and tenure.
4. Applied a chi-square test to investigate the association between contract type and churn.
5. Trained Logistic Regression and Random Forest models.
6. Evaluated classification performance and examined feature importance.
7. Generated churn-risk scores and segmented customers into low-, medium-, and high-risk groups.
8. Developed business recommendations from the findings.

## Logistic Regression Results

Test-set metrics:

Metrics:
Accuracy  0.726 
Precision  0.491
Recall  0.797 
F1-score  0.608 
ROC-AUC  0.835 

Class weighting was used to help identify customers likely to churn. Model thresholds and business trade-offs should be validated before deployment.

## Risk Segmentation

| Risk group | Customers | Actual churn rate |
|---|---:|---:|
| Low | 570 | 4.7% |
| Medium | 344 | 23.0% |
| High | 493 | 54.4% |

These results are from the held-out test sample. Risk thresholds are illustrative and do not guarantee future customer outcomes.

## Key Findings

- Tenure was the most important feature in the Random Forest model.
- Total charges and monthly charges were also prominent predictors.
- Contract type, internet service, and payment method contributed to model predictions.
- Actual churn rates increased across the low-, medium-, and high-risk groups.

## Business Recommendations

- Prioritize high-risk customers for retention outreach.
- Investigate onboarding and early-tenure customer experiences.
- Review contract options, pricing communication, and billing experiences.
- Investigate payment and technical-support friction.
- Evaluate retention campaigns through controlled pilots before estimating business impact.

## Limitations

Predictive relationships and feature importance do not establish causation. Risk thresholds are illustrative, and the analysis does not demonstrate that a retention campaign will reduce churn. Model performance should be evaluated on new data before operational use.


## Project Files

- `telecom_churn_analysis.ipynb` — data analysis and model development
- `telecom_churn_business_recommendations.csv` — business insights and recommendations
- `churn_risk_distribution.png` — customer risk group distribution
- `churn_rate_by_risk.png` — actual churn rate by risk group

