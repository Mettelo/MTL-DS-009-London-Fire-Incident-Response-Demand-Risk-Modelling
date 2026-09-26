# Required Deliverables

## D1 — Problem framing
Define:
- decision-support problem;
- user;
- target;
- modelling unit;
- success criteria;
- operational limitations.

Output:
`docs/01-problem-framing/`

## D2 — Data acquisition & understanding
Document:
- LFB incident data;
- LFB mobilisation data;
- periods used;
- keys;
- source grain;
- join logic;
- missing values;
- limitations.

Output:
`docs/02-data-understanding/`

## D3 — Incident-level modelling dataset
Build reproducible code that:
- loads both sources;
- joins on the correct incident key;
- aggregates mobilisation records;
- produces one row per incident;
- validates joins;
- generates the target.

Output:
`src/data/`

## D4 — Feature & leakage audit
Document every candidate feature and classify it as:
- allowed;
- excluded;
- uncertain/requires justification.

Explain why leakage-prone fields are excluded.

Output:
`docs/03-feature-and-leakage-audit/`

## D5 — Exploratory analysis
Analyse:
- target distribution;
- major incident categories;
- time patterns;
- geography where useful;
- missingness;
- target rates;
- drift/anomalies.

Output:
`docs/04-eda/`

## D6 — Baseline model
Implement and evaluate a transparent baseline.

## D7 — Candidate models
Compare at least two credible classification models.

Output:
`src/models/` and `docs/05-modelling/`

## D8 — Validation & threshold analysis
Report:
- precision;
- recall;
- F1;
- PR-AUC;
- ROC-AUC where useful;
- confusion matrices;
- threshold trade-offs;
- calibration where relevant.

Output:
`docs/06-evaluation-thresholds/`

## D9 — Explainability & error analysis
Provide:
- global model explanation;
- selected local explanations;
- false-positive analysis;
- false-negative analysis;
- performance by meaningful segments.

Output:
`docs/07-explainability-error-analysis/`

## D10 — Operational interpretation
Translate probabilities into documented analytical risk bands or planning outputs.

Do not represent them as official emergency-response decisions.

Output:
`docs/08-operational-interpretation/`

## D11 — Monitoring & technical handover
Document:
- setup;
- data refresh;
- model retraining;
- drift;
- performance monitoring;
- troubleshooting;
- limitations.

Output:
`docs/09-technical-handover/`

## D12 — Collaboration & submission
Complete:
- `CONTRIBUTIONS.md`;
- GitHub collaboration evidence;
- `submission/FINAL_SUBMISSION.md`;
- final tag.
