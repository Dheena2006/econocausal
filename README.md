# EconoCausal: Dynamic Pricing via Double Machine Learning

A reproducible Python/Jupyter research project exploring whether Double Machine Learning (DML) can estimate the effect of price on retail demand and inform pricing scenarios.

> **Research integrity:** This repository is a work in progress. Results will be reported only after running the analysis. A predictive score is not proof of causal validity. Public visibility does not mean that confidential internship material should be shared.

## Project status
**Milestone 0 — repository setup and research plan.** No model results are claimed yet.

## Research question
Can Double Machine Learning estimate the effect of product price on demand while adjusting for observed product, time, and promotion-related confounders, and can those estimates support economically meaningful pricing scenarios?

## Planned workflow
1. Define the estimand, unit of analysis, hypotheses, and identification assumptions.
2. Select and document a suitable public dataset and licence.
3. Download data reproducibly; retain raw data locally and out of version control unless redistribution is explicitly permitted.
4. Audit schema, missingness, outliers, price variation, time coverage, and sampling/selection limitations.
5. Conduct EDA and specify a defensible product-time panel if the data support one.
6. Build descriptive and predictive baselines with proper time-aware splits.
7. Fit a partially linear DoubleML model with cross-fitting; report estimate, standard error, confidence interval, and diagnostics.
8. Run robustness checks and discuss unobserved confounding, overlap/price support, and estimand limitations.
9. Build pricing scenarios only if the demand response and cost assumptions support them; distinguish revenue from profit.
10. Write results, limitations, reproducibility instructions, and final presentation.

## Dataset candidate
UCI Online Retail: https://archive.ics.uci.edu/dataset/352/online+retail

This is a candidate for initial data inspection, not an automatic guarantee of causal identification. It is transaction-level data and may not include zero-sales opportunities, all products/dates, or adequate confounders. Dataset suitability will be assessed before fitting DML. If it is unsuitable, the limitation will be documented and a better public panel dataset selected.

## Repository layout (planned)
```
data/raw/          # downloaded data (not committed)
data/processed/    # generated data (not committed unless small and permitted)
notebooks/         # sequential Jupyter analysis
outputs/figures/   # generated figures
outputs/evaluation/# generated estimates and metrics
docs/              # methodology, decisions, progress
```

## Reproducibility principles
- Record dataset source, access date, licence, schema, and preprocessing choices.
- Pin key Python dependencies.
- Set random seeds and document package versions.
- Use time-aware validation where observations are temporal; avoid leakage.
- Keep code and decisions in version control; do not commit secrets or confidential company documents.
- Report negative, inconclusive, and failed results honestly.

## Getting started
Python 3.11 is recommended.

```bash
python -m venv .venv
# Windows PowerShell:
.venv\Scripts\Activate.ps1
# macOS/Linux:
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
jupyter lab
```

## References
- DoubleML documentation: https://docs.doubleml.org/
- EconML documentation: https://econml.azurewebsites.net/
- UCI Online Retail dataset: https://archive.ics.uci.edu/dataset/352/online+retail

## Progress log
See [docs/PROGRESS.md](docs/PROGRESS.md) and the day-by-day plan in [docs/PROJECT_PLAN.md](docs/PROJECT_PLAN.md).
