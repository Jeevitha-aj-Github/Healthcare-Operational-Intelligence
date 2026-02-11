# Healthcare Operational Intelligence

Predicting 30 day hospital readmission risk using machine learning on structured EHR style data.  
Model objective: identify higher risk patients for early intervention.

## Dataset
- Diabetes 130 US hospitals dataset (101,766 encounters)
- Target: readmitted within 30 days (1) vs not within 30 days (0)

## Approach
- Cleaned data and created binary target (`<30` vs others)
- One hot encoded categorical variables
- Train test split: 80 20
- Baselines: Logistic Regression, Random Forest, Gradient Boosting
- Final model: XGBoost with small grid search and threshold tuning

## Results (Test Set)
- ROC AUC: ~0.68
- Example operating point (threshold tuned for F1): improves recall but reduces precision
- Business trade off: higher threshold increases precision (fewer false alarms) but misses more true readmissions

## Top Drivers (Model Features)
Common high impact factors included:
- number_inpatient
- discharge_disposition_id
- diagnosis codes (diag_1, diag_2, diag_3)

## Repository Structure
- `notebooks/` : data cleaning and model development notebooks

## How to Run
1. Install requirements
2. Open the notebook in `notebooks/`
3. Run cells top to bottom

## Notes
This is a learning project and not a clinical decision tool. Performance is moderate and should be improved with better feature engineering and calibration.


Specific diagnosis codes

Insight:
Prior healthcare utilization is the strongest indicator of early readmission, suggesting chronic high-use patients drive hospital penalty risk.
