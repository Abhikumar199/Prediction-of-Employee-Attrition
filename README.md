🧠 Employee Attrition Prediction
Machine Learning Techniques Project

Author: Abhishek Kumar


📌 Overview

Employee attrition significantly impacts organizational productivity, hiring cost, and long-term stability.
This project builds machine learning models to predict whether an employee is likely to leave based on HR analytics data (IBM HR Dataset).

The workflow includes:
✔ Exploratory Data Analysis (EDA)
✔ Data preprocessing
✔ Model development
✔ Model comparison
✔ Feature importance analysis



📂 Dataset

Dataset: IBM HR Analytics Employee Attrition Dataset

Rows: 1470

Columns: 35

Key features: Age, Monthly Income, Job Role, Job Satisfaction, Overtime, Tenure

Class Imbalance: Only ~16% employees have attrition → Requires metrics like Recall & Precision



🔍 Exploratory Data Analysis (Key Insights)

Employees doing OverTime have higher attrition.

Younger age group (25–35) shows more turnover.

Low job satisfaction strongly correlates with attrition.

Lower salary groups show higher attrition.

PCA and heatmaps show strong non-linear patterns → tree-based models perform well.

Dataset is highly imbalanced → Recall & Precision matter more than raw accuracy.



⚙️ Methodology
1. Data Cleaning

Removed irrelevant fields: EmployeeCount, StandardHours, Over18

No missing values

Duplicate rows removed (if any)

2. Feature Encoding

Label Encoding: Target (Attrition)

One-Hot Encoding: JobRole, Department, EducationField, etc.

3. Feature Scaling

StandardScaler for Logistic Regression

Tree models (RF & XGBoost) do not require scaling

4. Train/Test Split

80% train / 20% test

5. Models Used

Logistic Regression – baseline, interpretable

Random Forest Classifier

XGBoost Classifier



📊 Model Performance
Model	Accuracy	Recall	Precision	F1 Score
Logistic Regression	~80%	~72%	~42%	~53%
Random Forest	~80%	~54%	~41%	~47%
XGBoost	~85%	~37%	~50%	~42%


🔑 Interpretation

XGBoost achieved the highest accuracy.

Logistic Regression achieved the best recall and precision → Most reliable for predicting employees likely to leave.

Ensemble models (RF, XGBoost) captured non-linear patterns well but still didn’t match LR’s recall.




⭐ Most Important Features

OverTime

MonthlyIncome

JobRole

TotalWorkingYears

JobSatisfaction

Age

EnvironmentSatisfaction



🧾 Conclusion

The project successfully predicted employee attrition using ML models.
While XGBoost gave the highest accuracy, Logistic Regression performed best on Recall and Precision, making it more useful for HR teams to identify employees at risk and initiate interventions like:

improving job satisfaction

workload balancing

compensation adjustments



🚧 Limitations

Dataset is synthetic, not from a real organization

No psychological/external factors included

Class imbalance impacts performance




🚀 Future Enhancements

Apply SMOTE to balance the dataset

Use Deep Learning models

Deploy the model using Streamlit or Flask

Integrate SHAP for explainable AI

👤 Author

Abhishek Kumar
Machine Learning | Data Science | Artificial Intelligence
