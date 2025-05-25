# Code-for-Short--and-Long-Term-Outcomes-After-Abdominal-Aortic-Aneurysm-Repair

Purpose:
This repository delivers a fully automated machine‐learning pipeline designed to predict a comprehensive set of clinical outcomes following abdominal aortic aneurysm (AAA) repair. By leveraging the Vascular Quality Initiative’s multi‐center dataset, the workflow aims to generate accurate, calibrated risk estimates—ranging from perioperative endpoints such as 30-day mortality, myocardial infarction, and acute kidney injury to long-term metrics like one-year survival, aneurysm-related mortality, and reintervention rates. Ultimately, these models serve as decision‐support tools for clinicians and quality‐improvement teams seeking to benchmark performance and individualize patient care.

Inputs:
Outcome variables (e.g., MORTALITY_30DAY, MI_PERIOP, RENAL_FAILURE_NEW, etc.) and a rich set of predictors spanning preoperative (demographics, comorbidities, aneurysm anatomy), intraoperative (access site, graft details, procedural metrics), and immediate postoperative factors (ICU stay, complications). A compatible Python environment (3.7+) with the following libraries installed—pandas, numpy, scikit-learn, imbalanced-learn, xgboost, matplotlib, and seaborn—is required to execute the analysis.

Outputs:
Upon execution, the script prints cohort summaries (patient counts, repair types, rupture rate), training/testing splits, event rates, and model performance metrics (ROC-AUC, Brier score) directly to the console. It then generates publication-quality plots—ROC curves for all classifiers and calibration plots for the top model—along with a tabular summary comparing the best model per outcome against the logistic regression baseline. Subgroup analyses by age and aneurysm extent are also displayed, and a dedicated rupture analysis reports observed 30-day mortality for EVAR versus open repair in ruptured cases.

Constraints:
The pipeline assumes complete and correctly formatted data: all specified outcome and predictor columns must be present in the CSV. Hyperparameter tuning on a dataset of ~185,000 records can be computationally demanding; users may need to adjust CV folds, down-sample, or leverage distributed resources to fit within time and memory limits. Finally, the use of SMOTE to address class imbalance necessitates careful consideration of rare‐event definitions and oversampling parameters, as these choices directly influence model calibration and generalizability.





