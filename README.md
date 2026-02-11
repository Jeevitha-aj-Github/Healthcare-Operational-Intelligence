# Healthcare Operational Intelligence

## Project Overview

This project builds an end-to-end predictive analytics system to estimate 30-day hospital readmission risk and simulate operational cost trade-offs for healthcare decision-making.

The objective is not only to build a predictive model, but to evaluate its financial and operational deployment impact.

---

## Business Problem

Hospital readmissions within 30 days increase operational costs, strain clinical resources, and reduce quality-of-care metrics.

The goal is to:

- Predict high-risk patients at discharge
- Optimize intervention strategy using threshold tuning
- Quantify financial trade-offs between recall and precision

---

## Dataset

- 100,000+ patient encounters
- Clinical features (diagnoses, discharge disposition, inpatient history)
- Readmission target variable (binary classification)

---

## Modeling Approach

Models Evaluated:
- Logistic Regression
- Gradient Boosting
- XGBoost (final selected model)

Final Model:
- ROC AUC: **0.682**
- Optimized decision threshold: **0.20**

---

## Performance Trade-Off

Lower threshold:
- Higher recall
- More patients flagged
- Higher intervention cost

Higher threshold:
- Higher precision
- Fewer false positives
- Risk of missed readmissions

---

## Business Impact Simulation

Using cost assumptions:

- Cost of readmission: $15,000
- Cost of preventive intervention: $1,500

The model enables threshold-based financial strategy optimization.

---

## Repository Structure




Specific diagnosis codes

Insight:
Prior healthcare utilization is the strongest indicator of early readmission, suggesting chronic high-use patients drive hospital penalty risk.
