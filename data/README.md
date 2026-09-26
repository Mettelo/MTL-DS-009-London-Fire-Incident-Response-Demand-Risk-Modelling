# Data Sources

## Official source 1 — London Fire Brigade Incident Records
https://data.london.gov.uk/dataset/london-fire-brigade-incident-records-em8xy

This dataset contains incident-level information about incidents attended by London Fire Brigade.

## Official source 2 — London Fire Brigade Mobilisation Records
https://data.london.gov.uk/dataset/london-fire-brigade-mobilisation-records-24r65

This dataset contains mobilisation-level information about fire-engine deployments to incidents.

## Recommended project period
Use a manageable recent period.

Recommended:
- Incident data from 2024 onwards
- Mobilisation data from 2025 onwards

Teams may extend the period where useful and computationally practical.

## Core join requirement
Identify and validate the common incident identifier used across both datasets.

The final modelling dataset should contain **one row per incident**.

Mobilisation data should be aggregated before joining to the final model table.

## Target
Recommended starting target:

`high_response = 1 if appliance_mobilisations >= 3 else 0`

The exact threshold must be validated before final use.

## Leakage warning
Do not use the final appliance count itself—or other post-response information that directly reveals the outcome—as a predictive feature.

## Data handling
Do not commit large source files.

Store locally:

```
data/raw/
data/processed/
data/metadata/
```

## Metadata
Record:
- source URL;
- source file;
- source period;
- downloaded_at;
- raw row count;
- join key;
- join coverage;
- processing status;
- modelling version.
