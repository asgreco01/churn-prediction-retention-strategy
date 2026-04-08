# Customer Churn Prediction & Retention Strategy Optimization

## Overview

This project builds an end-to-end machine learning system to predict customer churn and translate predictions into actionable business strategies.

Beyond predictive modeling, the project focuses on:
- Identifying the key drivers of churn
- Explaining model decisions using SHAP
- Designing targeted retention strategies
- Estimating the financial impact of interventions (ROI simulation)

The goal is to bridge the gap between machine learning and real-world business decision-making.

## Business Problem

Customer churn is one of the most critical challenges for subscription-based businesses. Acquiring new customers is often more expensive than retaining existing ones.

This project answers three key questions:
1. Which customers are likely to churn?
2. Why are they likely to churn?
3. What actions should be taken to retain them profitably?

## Dataset

The project uses the Telco Customer Churn dataset, which contains information about customer demographics, account details, service usage, and churn status.

Key features include:
- Customer tenure
- Monthly and total charges
- Contract type
- Payment method
- Service subscriptions (e.g., internet, tech support, security)

Target variable:
- Churn (Yes / No)

## Methodology

### 1. Data Loading & Inspection
- Data validation and cleaning
- Handling missing values
- Type conversion (e.g., TotalCharges)

### 2. Exploratory Data Analysis (EDA)
- Churn distribution and class imbalance
- Feature distributions and segmentation
- Identification of churn drivers

### 3. Feature Engineering
- Tenure segmentation
- Customer value proxy (avg monthly value)
- Engagement score based on service usage
- Contract and payment behavior indicators

### 4. Modeling
- Logistic Regression (baseline model)
- Random Forest (non-linear model)
- Pipeline-based preprocessing (scaling, encoding, imputation)
- Evaluation using ROC-AUC, precision, recall

### 5. Model Explainability
- Feature importance (Random Forest)
- Coefficient analysis (Logistic Regression)
- SHAP values for global and local interpretability

### 6. Business Action Layer
- Risk segmentation (low, medium, high)
- Customer value segmentation
- Rule-based retention strategy assignment

### 7. ROI Simulation
- Estimation of intervention costs
- Expected retention success rates
- Calculation of expected saved value and net profit

## Key Findings

- Customers with short tenure are significantly more likely to churn
- Month-to-month contracts show the highest churn risk
- Higher monthly charges are associated with increased churn probability
- Customers with low engagement in additional services are more likely to leave

These patterns are consistent across EDA, model performance, and SHAP analysis.

## Business Recommendations

- Prioritize high-risk, high-value customers for retention efforts
- Strengthen onboarding and early customer engagement
- Incentivize long-term contracts over month-to-month plans
- Increase adoption of value-added services (e.g., tech support)
- Allocate retention budget based on expected ROI rather than uniform targeting

## ROI Impact

The project demonstrates how churn prediction can be translated into financial value by:

- Estimating the expected value of retained customers
- Comparing intervention costs vs. expected returns
- Identifying the most profitable retention strategies

Results show that a targeted retention approach can significantly outperform a non-targeted strategy.

## Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- SHAP

## Key Strengths

- End-to-end machine learning pipeline
- Strong focus on business applicability
- Model explainability (SHAP)
- Integration of analytics with financial decision-making
- Clear translation from prediction to action

## Limitations

- ROI simulation is based on simplified assumptions
- Real-world effectiveness depends on execution and customer behavior
- Dataset does not include behavioral or time-series dynamics

## Future Improvements

- Deploy the model as a real-time scoring system
- Integrate A/B testing for retention strategies
- Use advanced models (e.g., XGBoost, LightGBM)
- Incorporate behavioral and time-series features

## Final Note

This project demonstrates how machine learning can move beyond prediction and become a practical decision-making tool, directly supporting business strategy and customer retention efforts.
