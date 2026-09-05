# Reliable Structure–Processing–Performance Learning in Organic Photovoltaics

Reproducibility materials for the study **“Reliable Structure–Processing–Performance Learning in Organic Photovoltaics: Chemical Generalization, Processing-Aware Prediction and Uncertainty under Domain Shift.”**

**Author:** Dennis Obinna Orji  
**ORCID:** 0009-0009-1674-0883

## Study scope

This repository contains the computational workflow used to audit two literature-derived organic-photovoltaic datasets, define chemically independent validation regimes, evaluate structure- and processing-aware predictive models, diagnose domain shift, assess uncertainty reliability, audit cross-dataset representation compatibility, and generate the main publication figures and tables.

The repository is organized around three executed notebooks. Their original execution counters and scientific outputs are retained where appropriate, while personal email input, local machine paths, and a failed external-API test trace are removed from the public copies:

1. `01_data_audit_and_cohort_definition.ipynb` — provenance, integrity, identity, processing-data, cross-dataset and cohort audits.
2. `02_baseline_modelling_and_generalization.ipynb` — molecular representations, validation regimes, baseline/nonlinear models, processing-familiarity analysis, nested Ridge robustness, uncertainty, conformal intervals, transfer-feasibility audit and grouped permutation analysis.
3. `03_figures_and_manuscript_tables.ipynb` — generation of the six main figures and three main manuscript tables from frozen outputs.

## Source datasets

Raw third-party datasets are **not redistributed** in this repository. Obtain them from their original records and follow the license terms stated by the data providers.

- **OPV-DB (version used in this study):** Zenodo DOI `10.5281/zenodo.20841543`
- **Wen–Zhang–Ma OPV multi-tier processing dataset:** Zenodo DOI `10.5281/zenodo.17656284`

See `data/README.md` for the expected local directory structure.

## Reproduction order

Run the notebooks in numerical order. Notebook 01 creates the frozen cohorts and audit outputs used by Notebook 02. Notebook 02 creates the frozen modeling and reliability outputs used by Notebook 03. Notebook 03 should not modify the cohorts or fit new models.

Some provenance-enrichment steps in Notebook 01 use the Crossref API. The notebook caches retrieved metadata and requests a contact email for Crossref's polite API pool. The public copy does not contain the author's private input or local machine paths.

## Main outputs

The `figures/` directory contains the six main publication figures extracted from the frozen Notebook 03 outputs. The `tables/` directory contains the three main manuscript tables. Table 2 is published once as the canonical machine-readable CSV; manuscript formatting is handled separately.

## Environment

The recorded modeling environment used Python 3.11.15, NumPy 2.4.6, pandas 3.0.5 and scikit-learn 1.9.0. See `environment.yml` and `requirements.txt` for the main dependencies.

## Reproducibility notes

- Random validation is retained as an interpolation-oriented reference rather than described as universally invalid.
- Grouped validation prevents overlap only in the grouping variable defining each regime.
- Permutation importance is interpreted as predictive reliance, not causality.
- Extra Trees ensemble dispersion is treated as an uncertainty proxy, not as a universally calibrated epistemic uncertainty measure.
- The cross-dataset transfer-learning experiment was not forced because an independently generated common RDKit representation would selectively exclude modern high-performing acceptor chemistry.

## Citation

A `CITATION.cff` file is included. After the preprint is deposited, update the citation metadata with the ChemRxiv DOI and archived repository DOI.

## License

Code and original repository documentation are released under the MIT License. Third-party datasets and any content derived from them remain subject to the terms of their respective source records.
