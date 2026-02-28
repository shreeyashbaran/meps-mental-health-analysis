# Depression Insights from MEPS 2019 (ICD-10 F32)

**Data Analyst Portfolio Project** — Data merging • cleaning • feature engineering • EDA • insight storytelling

## What this project does (Quick scan)
Using U.S. **MEPS 2019** data, I built an analysis-ready dataset for individuals linked to **Depressive Episode (ICD-10: F32)** and explored how depression indicators vary by:
- **Region & gender**
- **Age groups**
- **Income / employment**
- **Race / ethnicity**
…and how severity relates to **healthcare expenditures**.

## Dataset
- Source: **Medical Expenditure Panel Survey (MEPS), AHRQ**
- Files used: **HC-214 (Conditions)** + **HC-216 (Full-Year Consolidated)**
- Merge key: **DUPERSID**
- Output: `data/aggregated.csv` → cleaned to `data/aggregated_cleaned.csv`

## Key outputs (what to look at)
- PHQ-2 and K6 distributions using clinical screening thresholds (PHQ-2 ≥ 4, K6 ≥ 13)
- Segment comparisons: region × gender, income groups, race/ethnicity
- Cost view: expenditure vs self-reported mental health

## How to run
### Fast path (recommended)
1. Install dependencies
2. Run: `notebooks/02_cleaning_feature_engineering_eda.ipynb`

### Full pipeline (rebuild merged dataset)
1. Download MEPS 2019 HC-214 + HC-216 (raw files not included here)
2. Run: `notebooks/01_build_dataset_meps_merge.ipynb`
3. Then run: `notebooks/02_cleaning_feature_engineering_eda.ipynb`

## Repo structure
- `notebooks/` → analysis workflow
- `data/` → processed datasets
- `reports/` → project writeups
- `figures/` → exported visuals (recommended)

## Notes / limitations
Observational survey data → insights are correlational (not causal). MEPS uses reserved negative codes for missing/inapplicable values; these were handled during cleaning.

---
If you’re reviewing quickly: open the EDA notebook and check `/figures` for the key plots.
