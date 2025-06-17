# Online Payment Fraud Detection using Machine Learning

![Fraud Detection](https://img.shields.io/badge/Fraud-Detection-red) ![Machine Learning](https://img.shields.io/badge/Machine-Learning-blue) ![Python](https://img.shields.io/badge/Python-3.8%2B-green)

This project focuses on detecting fraudulent online payment transactions using **Machine Learning** techniques. The goal is to classify transactions as **fraudulent** or **legitimate** with high accuracy while handling class imbalance and feature correlations.

## 📌 Table of Contents
- [Project Overview](#-project-overview)
- [Key Features](#-key-features)
- [Dataset](#-dataset)
- [Approach](#-approach)
- [Results](#-results)
- [Why Keeping Correlated Features Improved Performance?](#-why-keeping-correlated-features-improved-performance)
- [Potential Impact](#-potential-impact)


## 🔍 Project Overview
Online payment fraud is a major concern for businesses and consumers. This project:
- Preprocesses transaction data (handling missing values, scaling, etc.).
- Performs **feature selection** to identify key predictors of fraud.
- Tests multiple ML models (`Logistic Regression`, `Decision Trees`, `Naive Bayes`, `XGBoost`).
- Compares two approaches:  
  1. **Dropping one of two highly correlated features** (from heatmap).  
  2. **Keeping both correlated features** (surprisingly performed better).  

## 🎯 Key Features
- **Exploratory Data Analysis (EDA):** Visualizations (heatmaps, distributions) to understand data.
- **Model Comparison:** Evaluated precision, recall, F1-score, and AUC-ROC.
- **Best Model:** **Decision Tree** achieved the highest accuracy (~98%) when retaining correlated features.

## 📂 Dataset
- **Source:** [Kaggle / Financial Dataset](https://www.kaggle.com/datasets/ealaxi/paysim1](https://www.kaggle.com/datasets/jainilcoder/online-payment-fraud-detection))
- **Columns:**
  - `type` : Transaction Type. 
  - `amount`: Transaction amount.  
  - `oldbalanceOrg`, `newbalanceOrig`: Sender balances before/after transaction.  
  - `oldbalanceDest`, `newbalanceDest`: Receiver balances before/after transaction.  
  - `isFraud`: Binary label (0 = legitimate, 1 = fraud).  

## 🛠 Approach
1. **Data Preprocessing:**  
   - Handled missing values, normalized numerical features.  
   - Analyzed correlations (heatmap).  
2. **Feature Selection:**  
   - Used mutual information, correlation analysis.  
3. **Model Training:**  
   - Tested Logistic Regression, Decision Trees, Naive Bayes, XGBoost.    
4. **Two Experiments:**  
   - **Approach 1:** Dropped one of two highly correlated features.  
   - **Approach 2:** Kept both correlated features.  

## 📊 Results
| Model               | Precision | Recall | F1-Score | AUC-ROC |
|---------------------|-----------|--------|----------|---------|
| Logistic Regression | 84.10%      | 11.95%   | 20.93%     | 55.97%    |
| Decision Tree(with dropping correlated column)       | 64.39%      | 64.68%   | 64.54%     | 82.32%    |
| **Decision Tree (without Dropping)**         | **90.40%**  | **89.32**| **86.86%**| **94.66%**|

**Observation:** Keeping correlated features improved DT’s performance (see [explanation](#-why-keeping-correlated-features-improved-performance)).

## ❓ Why Keeping Correlated Features Improved Performance?
- **Tree-Based Models (XGBoost, DT)**: Can handle correlated features by splitting on either variable, capturing complementary signals.  
- **Information Redundancy**: Correlated features may encode subtle interactions (e.g., `oldbalanceOrg` and `newbalanceOrig` together indicate transaction patterns).  
- **Dropping Features**: May discard useful variance, especially if the correlation isn’t perfect (e.g., ρ = 0.9 ≠ 1.0).  

## 🌍 Potential Impact
- **Financial Loss Prevention:** Reduces revenue loss for businesses by flagging fraud in real time.  
- **Consumer Protection:** Prevents unauthorized transactions for users.  
- **Scalability:** Model can be deployed in payment gateways (e.g., Stripe, PayPal).  
- **Regulatory Compliance:** Helps meet anti-fraud standards (e.g., PSD2 in EU).  


