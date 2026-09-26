# Project Brief

## 1. Business context
Incident reporting tells planners what happened. A predictive risk model can help analysts identify which types of incidents are more likely to require a larger operational response and where operational pressure may be concentrated.

The project should support planning, analysis and resource-understanding use cases rather than live emergency dispatch.

## 2. Problem statement
Build a reproducible incident-level classification model using London Fire Brigade incident and mobilisation records.

The model should estimate the probability that an incident will require a higher operational response, while remaining explainable, appropriately validated and transparent about uncertainty and limitations.

## 3. Primary users
Assume the work supports:
- operational analytics teams;
- resource-planning teams;
- performance analysts;
- service-improvement teams;
- data science teams.

## 4. Target definition
Recommended starting target:

**High-response incident = 3+ appliance mobilisations**

The final threshold must be based on observed data distribution and documented rationale.

Teams must report:
- positive-class rate;
- negative-class rate;
- threshold rationale;
- sensitivity analysis if another threshold is plausible.

## 5. Unit of analysis
The final modelling table should contain **one row per incident**.

Mobilisation records must be aggregated to incident level before model training.

## 6. Data preparation requirements
Teams must:
- identify the incident key used across both datasets;
- validate join coverage;
- aggregate mobilisation records safely;
- remove duplicates;
- assess missing values;
- standardise categorical variables;
- parse date/time fields;
- engineer features only from information that would reasonably be available before or at the time of classification;
- explicitly identify and exclude leakage variables.

## 7. Leakage requirement
This is critical.

Do not use features that directly reveal the eventual response outcome.

Examples of likely leakage:
- final appliance count;
- response metrics generated after mobilisation;
- fields only known after the incident has progressed;
- derived variables that encode the target.

Every team must include a **feature-availability / leakage audit**.

## 8. Exploratory analysis
At minimum investigate:
- target balance;
- incident-category distribution;
- time-of-day patterns;
- day/month patterns;
- geography/borough patterns where appropriate;
- missingness;
- target rate by major categorical groups;
- feature distributions;
- potential outliers;
- temporal drift.

## 9. Baseline model
Implement at least one simple benchmark:
- majority-class baseline;
- simple logistic regression;
- or another transparent baseline.

## 10. Candidate models
Compare at least two credible models.

Examples:
- logistic regression;
- random forest;
- gradient boosting;
- XGBoost;
- LightGBM equivalent if available.

Do not select a model based only on accuracy.

## 11. Class imbalance
Assess whether imbalance materially affects the problem.

Possible approaches:
- class weights;
- threshold adjustment;
- resampling;
- precision-recall optimisation.

Do not apply SMOTE or another resampling technique automatically without justification.

## 12. Validation
Use a validation strategy appropriate for operational data.

Preferred:
- chronological train/validation/test split; or
- time-aware cross-validation where practical.

Random splitting may be used only if justified and compared against temporal validation.

## 13. Evaluation
Report metrics appropriate to the business problem, such as:
- precision;
- recall;
- F1;
- PR-AUC;
- ROC-AUC;
- confusion matrix;
- calibration metrics where relevant.

Accuracy alone is insufficient.

## 14. Threshold selection
Do not assume 0.50 is automatically the correct decision threshold.

Compare thresholds and explain the operational trade-off between:
- false negatives;
- false positives;
- recall;
- precision.

## 15. Explainability
Provide:
- global feature importance;
- local explanation examples where useful;
- SHAP or another suitable method;
- interpretation caveats.

Do not present associations as causal effects.

## 16. Error analysis
Analyse:
- false negatives;
- false positives;
- performance by key incident category;
- performance over time;
- any important subgroup differences.

## 17. Operational interpretation
Translate model outputs into a practical risk view.

Example:
- Low response-risk
- Medium response-risk
- High response-risk

These bands must be based on documented probability thresholds and must not be presented as official LFB operational categories.

## 18. Monitoring
Explain:
- data-drift checks;
- target-rate drift;
- model-performance monitoring;
- calibration monitoring;
- retraining/reselection triggers.

## 19. Out of scope
The core project does **not** require:
- live emergency dispatch;
- automated operational decisions;
- personal data;
- paid infrastructure;
- a production web application;
- causal inference.

## 20. Success definition
A reviewer should be able to clone the repository, obtain the documented public LFB data, reproduce the incident-level modelling table, train the models, evaluate them and regenerate the selected risk outputs without undocumented manual steps.
