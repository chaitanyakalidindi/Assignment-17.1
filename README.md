# Assignment-17.1
# Bank Marketing Campaign Analysis and Classification

# Project Overview

This project analyzes a dataset related to bank marketing campaigns to predict whether a client will subscribe to a term deposit. The goal is to build classification models that can identify high-propensity leads to improve marketing efficiency and ROI.

# Data

The dataset is sourced from the UCI Machine Learning Repository and contains information about bank clients, their contact history, and socio-economic factors.

# Analysis and Findings
The analysis involved:
Data Loading and Exploration: Understanding the features, identifying missing values (handled by dropping rows with 'unknown'), and visualizing distributions of key variables.
Feature Engineering: One-hot encoding was applied to categorical features, and some features with high multicollinearity or low correlation with the target variable were removed. Numerical features were scaled.
Baseline Model: A Dummy Classifier was used to establish a baseline Average Precision (PR-AUC) score.
Model Training and Comparison: Logistic Regression, K Nearest Neighbors (KNN), Decision Tree, and Support Vector Classifier (SVC) models were trained and tuned using Average Precision (PR-AUC) as the primary evaluation metric, which is suitable for the imbalanced dataset and aligns with the business objective of prioritizing positive cases.

# Model Performance (Average Precision - PR-AUC on Test Set):
| Model                  | Average Precision (PR-AUC) |
|-------------------------|-----------------------------|
| Logistic Regression     | ~0.60                       |
| Decision Tree (pruned)  | ~0.52                       |
| SVC (RBF)               | ~0.51                       |
| KNN                     | ~0.47                       |


The Logistic Regression model demonstrated the best performance in terms of Average Precision, indicating its effectiveness in ranking clients most likely to subscribe higher. This is a significant improvement over the baseline (which would be the prevalence of the positive class).

# Conclusion and Recommendations

The Logistic Regression model is the most promising for predicting term deposit subscriptions based on the current analysis. Further improvements could involve more extensive feature engineering, exploring other advanced models (e.g., Gradient Boosting), addressing class imbalance more explicitly, and evaluating models without the 'duration' feature for a truly predictive scenario before a call.

# Notebook
You can access the full analysis and code in the following Jupyter Notebook:

[Link to the Notebook - Replace with actual link]
