This project aims to identify signs of depression among students using survey data and machine learning. 
The goal is to leverage data-driven insights to better understand factors contributing to student mental health struggles and build predictive models that can help early identification.

# **Technology Used**:
1. Python (Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib)

2. Machine Learning: Random Forest, SVM, XGBoost

3. Feature Engineering

4. Exploratory Data Analysis (EDA)

5. Model Evaluation: ROC-AUC, F1-score, Classification Report

# **Dataset Overview**:

The dataset contains responses from ~28,000 students, with features like:

🎓 Academic Pressure, CGPA, Study Satisfaction

💤 Sleep Duration

🧠 Suicidal Thoughts, Family History

🍎 Dietary Habits, Financial Stress

🕒 Work/Study Hours

🧑 Gender, Age, Degree

🎯 Target: Depression (0 = No, 1 = Yes)


# 🔍 **Key Steps**:

📌 1. Data Cleaning & Preprocessing
Removed irrelevant columns like Profession, City

Encoded categorical variables

Handled missing values

📌 2. Feature Engineering
✅ Stress Index = Academic Pressure - Study Satisfaction

✅ CGPA Risk Score to map academic performance to stress

✅ Age Grouping (Teens, Early 20s, etc.)

📌 3. Exploratory Data Analysis (EDA)
Visualized depression vs CGPA, Sleep, Degree, etc.

## Insights:

Higher academic pressure & low study satisfaction → higher depression

Students with <5 hrs of sleep or financial stress showed elevated risk

📌 4. Model Building
Random Forest: Accuracy ~85%, ROC-AUC ~0.91

# 💡 **What Makes This Project Unique?**:

1. Strong feature engineering that captures psychological dimensions (like stress)

2. Deep EDA with storytelling visuals

3. Clean pipeline for scaling, encoding, and modeling

4. Interpretable models + solid performance

5. SVM: Also performed well with linear and RBF kernels

6. XGBoost: Fast, robust results

7. Compared models using classification reports & ROC curves
