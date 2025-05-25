# Code-for-Short--and-Long-Term-Outcomes-After-Abdominal-Aortic-Aneurysm-Repair

Purpose:
To implement an end-to-end machine-learning workflow that ingests real-world VQI data on abdominal aortic aneurysm (AAA) repairs and delivers validated risk-prediction models for both short-term (e.g., 30-day mortality, myocardial infarction, acute kidney injury) and long-term outcomes (e.g., 1-year survival, endoleak, reintervention). The goal is to provide clinicians and quality-improvement teams with calibrated decision-support tools and clear performance reporting.

Inputs:

A CSV file named vqi_aaa_data.csv containing:

Outcome columns:

MORTALITY_30DAY, MI_PERIOP, RENAL_FAILURE_NEW, SPINAL_CORD_ISCHEMIA,

ISCHEMIC_COLITIS, BUTTOCK_CLAUDICATION, MAJOR_COMPLICATIONS, PROLONGED_LOS,

OVERALL_SURVIVAL_1YR, AAA_RELATED_MORTALITY, REINTERVENTION, ENDOLEAK,

GRAFT_INFECTION, RUPTURE_RELATED_MORTALITY

Predictor columns (preop, intraop, postop as defined in the script)

Python environment with the required libraries installed:
pandas, numpy, scikit-learn, imbalanced-learn, xgboost, matplotlib, seaborn

Outputs:

Console logs summarizing cohort characteristics, training/test splits, event rates, and model metrics.

Tabular summary of best-performing models per outcome (AUC, Brier score, improvement over logistic regression).

Publication-quality Matplotlib figures:

ROC curves for all classifiers

Calibration plots for the top model

Subgroup AUC analyses by age (<70 vs. ≥70) and aneurysm extent (infrarenal vs. juxta/para/suprarenal).

Separate mortality comparison for ruptured EVAR vs. open repair cases.

Constraints:

Data completeness: All specified columns must be present and free of critical formatting errors.

Memory/compute: Hyperparameter tuning on ~185k rows can be time- and memory-intensive; consider down-sampling or distributed compute if needed.

Software versions: Tested on Python 3.7+; dependency versions should match those in requirements.txt.

Imbalance handling: SMOTE is applied for rare outcomes—results depend on appropriate class-imbalance settings.











