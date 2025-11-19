# Customer Lifetime Value (CLV) Prediction Project

## Project Overview

This project demonstrates an end-to-end analytics pipeline to predict customer lifetime value (CLV) based on historical transaction behaviour. The goal is to enable businesses (including credit / fraud risk teams) to segment customers by long-term value and tailor strategies for retention, cross-sell, and risk-profiling.

## Business Problem

In competitive financial and e-commerce markets, understanding which customers generate the highest lifetime value is critical. For a company like American Express, segmentation and prediction of customer value enables optimized credit risk assessment, targeted marketing, and improved portfolio profitability. By using RFM segmentation and machine-learning classification, the model enables proactive strategy rather than reactive response.

## Data & Feature Engineering

- Transactions data is processed to compute key features:
  - **Recency**: number of days since last purchase
  - **Frequency**: number of purchases in observation window
  - **Monetary**: average or total spend
- Data cleaning and preprocessing steps include handling missing values, filtering active customers, scaling continuous features, and encoding categorical variables as needed.
- Clustering (K-Means) is used to derive customer value segments (e.g., low, medium, high). These clusters form the target labels for classification.

## Modeling Approach

1. **Segmentation**: K-Means clustering on RFM features to categorize customers into 3 distinct value segments.
2. **Classification**: XGBoost classifier trained to predict a customer’s segment (i.e., future lifetime-value tier) based on historical features.
3. **Evaluation**: Standard classification metrics (accuracy, precision, recall, F1) and confusion-matrix analysis are used to validate model performance.
4. **Insights**: Feature importance is examined to uncover the highest-impact attributes driving customer lifetime value.

## Key Results & Insights

- Successfully segmented customers into three tiers using K-Means, enabling differentiated business strategy.
- The classification model demonstrated robust predictive capability for value-tier assignment (details in notebook).
- Insights revealed that recency and frequency were dominant drivers of value-tier classification — critical for retention and credit-risk strategy.
- The pipeline is structured to be extensible to credit/fraud risk domains (e.g., combining behavioural features with value segmentation, enabling targeted risk scoring and resource allocation).

## Technologies Used

- Programming: Python (Jupyter Notebook)
- Libraries: Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn
- Workflow: Git/GitHub for version control
- Methods: RFM feature engineering, K-Means clustering, gradient-boosted classification, evaluation metrics

## How to Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/adesh-k-patra/clv-prediction.git
   ```
