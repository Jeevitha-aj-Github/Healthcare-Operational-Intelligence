Predicting 30-Day Hospital Readmission Risk

Objective:
Identify patients at high risk of readmission within 30 days using structured hospital encounter data.

Dataset:
101,766 diabetic patient encounters from US hospitals.

Modeling Approach:

Baseline: Logistic Regression

Boosting Models: Gradient Boosting & XGBoost

Hyperparameter tuning via GridSearch

ROC AUC used as primary evaluation metric

Best Model Performance:

ROC AUC: 0.682

Optimal threshold balancing recall and precision

Key Predictors Identified:

Prior inpatient visits (strongest signal)

Discharge disposition

Specific diagnosis codes

Insight:
Prior healthcare utilization is the strongest indicator of early readmission, suggesting chronic high-use patients drive hospital penalty risk.
