# Mandatory Team Repository Structure

Each team must create a separate repository named:

`MTL-DS-009-<team-name>`

Minimum structure:

```
MTL-DS-009-<team-name>/
│
├── README.md
├── CONTRIBUTIONS.md
├── requirements.txt
├── .gitignore
│
├── data/
│   ├── raw/
│   │   └── README.md
│   ├── processed/
│   │   └── README.md
│   └── metadata/
│       └── README.md
│
├── docs/
│   ├── 01-problem-framing/
│   │   └── README.md
│   ├── 02-data-understanding/
│   │   └── README.md
│   ├── 03-feature-and-leakage-audit/
│   │   └── README.md
│   ├── 04-eda/
│   │   └── README.md
│   ├── 05-modelling/
│   │   └── README.md
│   ├── 06-evaluation-thresholds/
│   │   └── README.md
│   ├── 07-explainability-error-analysis/
│   │   └── README.md
│   ├── 08-operational-interpretation/
│   │   └── README.md
│   └── 09-technical-handover/
│       └── README.md
│
├── src/
│   ├── data/
│   ├── features/
│   ├── models/
│   ├── evaluation/
│   ├── explainability/
│   └── utils/
│
├── notebooks/
├── tests/
├── models/
├── outputs/
│   ├── predictions/
│   ├── figures/
│   └── tables/
│
└── submission/
    └── FINAL_SUBMISSION.md
```

## Repository rules

### Raw data
Do not commit large LFB source files.

Provide:
- official source links;
- reproducible download instructions;
- processing code;
- metadata.

### Notebook rule
Use notebooks for exploration, not as the entire production workflow.

Reusable logic must be moved into `src/`.

### Model artifacts
Commit only small model artifacts when useful.

### Collaboration evidence
Use:
- issues;
- feature branches;
- meaningful commits;
- pull requests;
- peer review.

## Final version
After QA and Mettelo review:

`v1.0-mettelo-submission`
