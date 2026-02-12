Good. I’ll give you a clean, final, ready-to-paste version. No fluff. Professional. Structured.

Copy this exactly.

Healthcare Operational Intelligence

Predicting 30-Day Hospital Readmission & Simulating Business Impact

Executive Summary

Built a healthcare operational analytics solution to support hospital leadership in reducing 30-day readmission penalties.
Combined risk modeling, SQL-driven KPI extraction, and cost simulation to evaluate intervention strategies.
Designed as a decision-support framework linking discharge risk scoring to measurable financial outcomes.

Business Problem

30-day readmissions increase hospital penalties and operational burden.

Key questions addressed:

Can high-risk patients be identified before discharge?

Which variables drive readmission risk?

How does threshold selection affect financial trade-offs?

What is the estimated monetary impact of intervention?

Operational Workflow

Risk score is generated at the time of discharge.
Patients above the selected threshold are flagged for care coordination review.
Flagged patients are assumed to receive preventive intervention (post-discharge follow-up, medication review, care plan reinforcement).
Monthly flagged patient count is translated into intervention cost.
Prevented readmissions are translated into avoided penalty cost.
Net financial impact is calculated for hospital leadership decision making.

Dataset

100,000+ patient encounters

2,400+ engineered features after encoding

Binary target: 30-day readmission (<30 days)

Preprocessing included:

Categorical encoding

Feature engineering

Train-test split (80/20)

Class imbalance handling

Threshold optimization

Modeling Approach

Models evaluated:

Logistic Regression

Gradient Boosting

XGBoost (selected final model)

Model selection included hyperparameter tuning using cross-validation.
Primary evaluation metric: ROC-AUC.

Final Model Performance

Best Test ROC-AUC: 0.682

Selected Threshold: 0.20

Classification performance at threshold 0.20:

Accuracy: 85%

Recall (High-risk patients): 23%

Precision (High-risk predictions): 28%

Model performance prioritizes financial efficiency over maximum recall, aligning threshold selection with budget-constrained intervention strategy.

Threshold Sensitivity Analysis
Threshold	Recall	Precision	Estimated Net Savings
0.15	X%	X%	₹X
0.20	23%	28%	₹17.13M
0.25	X%	X%	₹X

Lower thresholds increase patient coverage but raise intervention costs.
Higher thresholds reduce intervention cost but may miss high-risk patients.
Threshold selection should align with hospital budget constraints and care capacity.

Key Insight

Top Feature by Importance:
Number of previous inpatient visits

This highlights prior hospital utilization as the strongest operational signal for future readmission risk.

Business Impact Results

At a 0.20 risk threshold:

Readmissions Prevented: 528

Intervention Cost Assumed: ₹5,000 per flagged patient

Readmission Cost Assumed: ₹50,000 per case

Estimated Net Savings: ₹17.13 Million

This simulation illustrates how threshold-based risk stratification can influence hospital cost structure and intervention allocation.

Assumptions

Intervention success rate assumed constant across flagged patients

Average intervention cost assumed at ₹5,000 per patient

Average readmission cost assumed at ₹50,000 per case

Costs treated as fixed and not department specific

Model performance assumed stable over time (no drift modeled)

Limitations

Model not externally validated on independent hospital dataset

No real-time deployment architecture implemented

Demographic bias and fairness analysis not performed

Savings simulation does not account for behavioral or operational variability

Feature importance interpretation reflects association, not causation

Repository Structure

notebooks/
    data_cleaning.ipynb
    modeling.ipynb
    business_impact_simulation.ipynb

README.md

Technology Stack

Python (pandas, numpy, scikit-learn, XGBoost)
SQL (multi-table joins, cohort analysis, rolling 30-day metrics, KPI extraction)
Power BI (executive-level operational dashboard)
Jupyter Notebooks

Capabilities Demonstrated

Healthcare operational KPI design
Risk threshold decision analysis
Cost–benefit modeling aligned to hospital budgets
SQL-based cohort and readmission rate calculation
Executive-level data storytelling
Structured analytical documentation with stated assumptions and limitations

