# Acceptance Criteria

## Problem framing
- User and decision-support purpose are clear.
- Target is explicit.
- Target threshold is justified from the data.
- Unit of analysis is one row per incident.

## Data
- Official LFB sources are used.
- Incident and mobilisation datasets are both incorporated.
- Join key and join coverage are documented.
- Large raw files are not committed.
- Data limitations are documented.

## Reproducibility
- A reviewer can reproduce the modelling dataset.
- Paid services are not required.
- Local paths are portable/configurable.

## Leakage
- Feature-availability audit exists.
- Target leakage is explicitly assessed.
- Post-outcome fields are excluded where necessary.

## EDA
- Target balance assessed.
- Major feature distributions assessed.
- Missingness assessed.
- temporal patterns/drift considered.
- No unsupported causal claims made.

## Baseline
- Transparent baseline implemented.
- Baseline performance reported.

## Modelling
- At least two credible models compared.
- Model choice justified by evidence.
- Class imbalance handled appropriately where needed.

## Validation
- Appropriate holdout/validation design used.
- Precision and recall reported.
- F1 and PR-AUC reported.
- Accuracy is not used alone.
- Threshold analysis completed.
- Calibration assessed where relevant.

## Explainability
- Global explanation provided.
- Interpretation does not imply causation.
- Local explanations used where useful.

## Error analysis
- False positives analysed.
- False negatives analysed.
- Segment/time performance assessed.

## Operational interpretation
- Probability/risk bands are documented.
- Risk bands are clearly analytical, not official LFB dispatch categories.
- Limitations clearly stated.

## Engineering quality
- Reusable code exists outside notebooks.
- Functions/modules are readable.
- Dependencies reproducible.
- Important data/model logic tested.
- No sensitive data/secrets committed.

## Documentation
- Setup complete.
- Data acquisition documented.
- Target documented.
- Leakage decisions documented.
- Model selection documented.
- Monitoring/retraining documented.

## Collaboration
- Contributions transparent.
- Git history shows meaningful participation.
- PR workflow used where practical.

## Submission
- Final submission complete.
- Reviewer has access.
- QA complete.
- Final tag `v1.0-mettelo-submission` created.
