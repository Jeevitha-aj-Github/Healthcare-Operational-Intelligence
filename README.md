Healthcare Operational Intelligence

Predicting 30-Day Hospital Readmission & Simulating Business Impact

Project Overview

This project analyzes 30-day hospital readmission risk using real-world healthcare data and demonstrates how predictive modeling translates into measurable operational cost savings.

The goal is not just model accuracy — but operational decision support.

Business Problem

Hospital readmissions within 30 days increase financial penalties and strain hospital resources.

Key questions addressed:

Can high-risk patients be identified before discharge?

Which operational factors drive readmission risk?

How does classification threshold impact business trade-offs?

What is the financial impact of preventive interventions?

Dataset

100,000+ patient encounters

2,400+ engineered features after encoding

Binary target: 30-day readmission (<30 days)

Preprocessing steps:

Categorical encoding

Feature engineering

Train-test split (80/20)

Class imbalance handling

Threshold optimization

Modeling Approach

Models evaluated:

Logistic Regression

Gradient Boosting

XGBoost (final selected model)

Model selection method:

GridSearchCV (3-fold cross-validation)

Evaluation metric: ROC-AUC

Final Model Performance

Best Test ROC-AUC: 0.682

Selected Threshold: 0.20

Classification performance at threshold 0.20:

Accuracy: 85%

Recall (High-risk patients): 23%

Precision (High-risk predictions): 28%

This reflects the operational trade-off between identifying more at-risk patients and minimizing false positives.

Key Insight

Strongest readmission predictor:

Number of previous inpatient visits

This confirms prior hospital utilization as the dominant operational signal for future readmission risk.

Business Trade-Off Analysis

Lower Threshold:

Higher recall

More patients flagged

Higher intervention cost

Higher Threshold:

Higher precision

Fewer patients flagged

Lower operational cost

The model enables hospitals to align predictive decisions with financial strategy.

Business Impact Simulation

A cost simulation framework evaluates:

Cost per readmission

Cost per preventive intervention

Net savings under different threshold strategies

This transforms predictive modeling into actionable operational intelligence.

Repository Structure

notebooks/

data_cleaning.ipynb

modeling.ipynb

business_impact_simulation.ipynb

README.md

Technology Stack

Python (pandas, numpy, scikit-learn, XGBoost)

SQL (data logic representation)

Power BI (dashboard visualization)

Jupyter Notebooks

Project Capabilities Demonstrated

End-to-end ML workflow

Imbalanced classification handling

Hyperparameter tuning

Threshold optimization

Business-aligned evaluation

Operational cost reasoning




Specific diagnosis codes

Insight:
Prior healthcare utilization is the strongest indicator of early readmission, suggesting chronic high-use patients drive hospital penalty risk.
