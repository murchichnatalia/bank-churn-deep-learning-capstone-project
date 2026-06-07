# Bank Customer Churn Prediction with Deep Neural Networks

## Project Overview

This capstone project develops a deep neural network model for predicting bank customer churn.

Customer churn is a major challenge for financial institutions, because losing existing customers directly affects revenue, customer lifetime value, and marketing costs. The goal of this project is to identify customers with a high probability of churn and support proactive retention strategies.

The project is based on the Bank Customer Churn Dataset from Kaggle.

## Business Problem

The model predicts whether a customer is likely to leave the bank based on customer-level data, including demographic information, financial indicators, product usage, and engagement features.

This can help a bank detect early churn signals and launch targeted retention campaigns.

## Dataset

The project uses the Bank Customer Churn Dataset.

Main features include:

- Customer demographics
- Geography and gender
- Credit score
- Age
- Balance
- Number of products
- Credit card ownership
- Active membership status
- Estimated salary
- Exited target variable

Important note: the dataset does not contain explicit time-series data. In real banking systems, churn prediction is often based on transaction history and behavioral sequences. However, due to confidentiality restrictions, real production-level data from banks such as Sberbank cannot be used. Therefore, this dataset is treated as a proxy for aggregated customer behavior.

## Modeling Approach

The main model is a Deep Multilayer Perceptron (Deep MLP).

Architecture:

- Input layer with normalized customer features
- Dense layers: 64 → 32 → 16 neurons
- ReLU activation
- Dropout regularization
- Sigmoid output layer for churn probability
- Weighted Binary Cross-Entropy to focus on churn cases

The model is suitable for this dataset because the data is tabular and non-sequential. The bottleneck structure helps the neural network learn a compact representation of customer behavior.

## Evaluation Metrics

The main evaluation metric is ROC-AUC.

Additional metrics:

- Precision
- Recall
- F1-score

Recall is especially important because missing a customer who is likely to churn is costly for the business.

## Repository Structure

```text
bank-churn-deep-learning-capstone/
│
├── Bank_Churn_Capstone_Project_team11.ipynb
├── README.md
├── requirements.txt
├── data/
│   └── Churn_Modelling.csv
└── outputs/
