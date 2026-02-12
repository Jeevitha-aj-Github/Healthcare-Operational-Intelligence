# Healthcare Operational Intelligence  
Predicting 30-Day Hospital Readmission & Simulating Business Impact

---

## Project Overview

This project predicts 30-day hospital readmission risk and quantifies the financial impact of preventive intervention strategies.

This project demonstrates how machine learning can be integrated into hospital decision workflows to reduce readmission penalties and optimize intervention spending.

The objective is not just model accuracy, but operational decision support.

---

## Business Problem

30-day readmissions increase hospital penalties and operational burden.

Key questions addressed:

- Can high-risk patients be identified before discharge?
- Which variables drive readmission risk?
- How does threshold selection affect financial trade-offs?
- What is the estimated monetary impact of intervention?

---

## Dataset

- 100,000+ patient encounters  
- 2,400+ engineered features after encoding  
- Binary target: 30-day readmission (<30 days)

Preprocessing included:

- Categorical encoding  
- Feature engineering  
- Train-test split (80/20)  
- Class imbalance handling  
- Threshold optimization  

---

## Modeling Approach

Models evaluated:

- Logistic Regression  
- Gradient Boosting  
- XGBoost (selected final model)  

Model selection:

- GridSearchCV (3-fold cross-validation)  
- ROC-AUC as evaluation metric  

---

## Final Model Performance

Best Test ROC-AUC: 0.682

Selected Threshold: 0.20

Classification performance at threshold 0.20:

- Accuracy: 85%  
- Recall (High-risk patients): 23%  
- Precision (High-risk predictions): 28%  

This reflects the trade-off between identifying more at-risk patients and minimizing false positives.

---

## Key Insight

Strongest readmission predictor:

Number of previous inpatient visits

This confirms prior hospital utilization as the dominant operational signal for future readmission risk.

---

## Business Impact Results

At a 0.20 risk threshold:

- Readmissions Prevented: 528  
- Intervention Cost Assumed: ₹5,000 per flagged patient  
- Readmission Cost Assumed: ₹50,000 per case  
- Estimated Net Savings: ₹17.13 Million  

This demonstrates how predictive modeling directly translates into measurable financial savings.

---

## Repository Structure

notebooks/
    data_cleaning.ipynb
    modeling.ipynb
    business_impact_simulation.ipynb

README.md

---

## Technology Stack

- Python (pandas, numpy, scikit-learn, XGBoost)
- SQL (data logic representation)
- Power BI (dashboard visualization)
- Jupyter Notebooks

---

## Capabilities Demonstrated

- End-to-end ML workflow  
- Imbalanced classification handling  
- Hyperparameter tuning  
- Threshold optimization  
- Business-aligned evaluation  
- Financial impact simulation  


