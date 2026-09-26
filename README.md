# MTL-DS-009 — London Fire Incident Response Demand & Risk Modelling

## Project title
**London Fire Incident Response Demand Classification & Operational Risk Modelling**

## Project type
Data Science · Team project · Production-style portfolio project

## Challenge
London Fire Brigade publishes incident-level and mobilisation-level operational data covering incidents attended and appliance deployments.

A planning and analytics team wants a model that can identify incidents associated with a higher operational response requirement and explain the factors linked with that classification.

Your team will build that classification and operational-risk modelling workflow.

## Official data sources

London Fire Brigade Incident Records:

https://data.london.gov.uk/dataset/london-fire-brigade-incident-records-em8xy

London Fire Brigade Mobilisation Records:

https://data.london.gov.uk/dataset/london-fire-brigade-mobilisation-records-24r65

## Recommended data scope
Use a manageable recent period rather than the entire historical archive.

Recommended:
- Incident records from **2024 onwards**
- Mobilisation records from **2025 onwards**

Teams may extend the period where technically appropriate, but the project must remain practical to run on a normal laptop.

## Cost requirement
**The complete project must be achievable at £0.**

Recommended free stack:
- Python
- pandas
- NumPy
- scikit-learn
- XGBoost or LightGBM equivalent if desired
- SHAP
- matplotlib
- Jupyter
- Git
- GitHub

No paid infrastructure or deployment service is required.

## Core modelling problem
Build a classification model that estimates whether an incident is likely to require a higher operational response.

Recommended initial target definition:

**High-response incident = incident associated with 3 or more appliance mobilisations**

The team must validate the target distribution before finalising this threshold.

If the distribution shows that another threshold is more operationally meaningful, the team may change it, but the final definition must be:
- justified;
- documented;
- reproducible;
- applied consistently.

## Core objective
Build a reproducible data science workflow that:

1. acquires and combines incident and mobilisation data;
2. constructs an incident-level analytical dataset;
3. defines and validates a classification target;
4. investigates class balance and leakage risks;
5. creates a transparent baseline model;
6. compares at least two credible classification approaches;
7. evaluates performance using suitable imbalance-aware metrics;
8. calibrates or assesses predicted probabilities where appropriate;
9. selects an operationally meaningful decision threshold;
10. explains model behaviour and important drivers;
11. performs error analysis;
12. translates outputs into a practical operational-risk view;
13. documents monitoring and retraining requirements.

## Required analytical flow

```
LFB incident data + mobilisation data
        ↓
Join & incident-level feature construction
        ↓
Target definition
        ↓
Data-quality checks
        ↓
EDA & class-balance analysis
        ↓
Baseline classifier
        ↓
Candidate models
        ↓
Validation & threshold analysis
        ↓
Explainability
        ↓
Error analysis
        ↓
Operational interpretation
```

## Business questions
The solution should help answer:

- Which incidents are more likely to require a higher appliance response?
- Which incident, time and location features are most associated with higher response demand?
- How accurately can the model identify higher-response incidents?
- What is the trade-off between missing a high-response incident and creating too many false alerts?
- What probability threshold is appropriate for a planning/risk use case?
- Where does the model perform poorly?
- How stable are predictions across incident categories or time periods?

## Important modelling rule
This project is about **decision support**, not automating emergency dispatch.

Do not describe the model as replacing London Fire Brigade operational judgement, control-room processes or emergency-response procedures.

## Team submission model
Each team creates **its own GitHub repository**.

Recommended naming:

`MTL-DS-009-<team-name>`

The Mettelo repository is the project specification.

Each team must:
1. create its own repository;
2. invite the designated Mettelo reviewer/collaborator;
3. follow `project/REPOSITORY_STRUCTURE.md`;
4. use issues/branches/commits/pull requests as evidence of collaboration;
5. complete `submission/FINAL_SUBMISSION.md`;
6. complete final QA;
7. tag the accepted version `v1.0-mettelo-submission`;
8. submit the repository URL.

## Project documents
- [Project brief](project/PROJECT_BRIEF.md)
- [Data guidance](data/README.md)
- [Mandatory repository structure](project/REPOSITORY_STRUCTURE.md)
- [Deliverables](project/DELIVERABLES.md)
- [Acceptance criteria](project/ACCEPTANCE_CRITERIA.md)
- [Team roles](project/TEAM_ROLES.md)
- [Contribution rules](CONTRIBUTIONS.md)
- [Final submission template](submission/FINAL_SUBMISSION.md)

---
**Mettelo — Built for What’s Next**
