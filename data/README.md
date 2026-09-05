# Data setup

Raw source datasets are not included. Download them from the original source records and preserve their original license notices.

Expected project layout used by the notebooks:

```text
data/
├── raw/
│   ├── opvdb/
│   └── opv-multi-tier-ml-database/
├── interim/
└── processed/
```

Notebook 01 creates the provenance-clean OPV cohort, the physically harmonized Wen–Zhang–Ma cohort, feature manifests and validation-group metadata under `interim/`. Notebook 02 writes frozen model, reliability, uncertainty, transfer-audit and grouped-permutation outputs under `processed/`. Notebook 03 reads these frozen files and creates figures/tables.

Source records:

- OPV-DB: https://doi.org/10.5281/zenodo.20841543
- Wen–Zhang–Ma dataset: https://doi.org/10.5281/zenodo.17656284

Do not substitute a newer dataset release without re-running the full audit, because the manuscript results correspond to the versions audited in this study.
