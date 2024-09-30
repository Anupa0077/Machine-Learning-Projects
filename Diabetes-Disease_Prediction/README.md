

---

# Diabetes Prediction Project

## Overview
This project aims to predict diabetes using the Pima Indians Diabetes Dataset. The project involves data preprocessing, training a Support Vector Machine (SVM) model with different kernels, and evaluating the model's performance using various metrics, including recall score.

## Project Steps

### 1. Data Preprocessing
- **Loading Data**: The dataset was loaded using pandas.
- **Handling Missing Values**: Missing values were handled by imputing with the median of each column.
- **Feature Scaling**: StandardScaler was used to standardize the features.

### 2. Model Training
- **Support Vector Machine (SVM)**: An SVM classifier was used to predict diabetes.
- **Kernel Selection**: Different kernels (linear, polynomial, RBF) were tested to determine the best performing model.


### 3. Model Evaluation
- **Metrics**: The models were evaluated using accuracy, precision, recall, and F1 score.
- **Recall Score**: Special attention was given to the recall score to ensure that the model effectively identifies positive cases of diabetes.

## Results
- **Best Kernel**: The Linear kernel SVM achieved the highest accuracy score.
- **Performance Metrics**: 
  - **Accuracy**: 0.80
    
  **Class 0**: Represents the non-diabetic cases.
     - **Precision**: 0.89
    - **Recall**: 0.79
    - **F1-Score**: 0.84
      
  **Class 1**: Represents the diabetic cases.
    - **Precision**: 0.67
    - **Recall**: 0.81
    - **F1-Score**: 0.74
