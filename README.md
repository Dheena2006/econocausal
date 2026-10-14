# EconoCausal: Dynamic Pricing via Double Machine Learning

**Internship project | Python | Jupyter Notebook | 10-day incremental build**

## Objective
Evaluate whether a public retail dataset can support a defensible estimate of how product price affects demand using Double Machine Learning (DML), and whether that estimate can responsibly inform economic pricing scenarios.

## Research workflow
1. Select a public dataset and record source, licence and schema.
2. Load it reproducibly; audit missing, invalid, duplicate and extreme records.
3. Perform exploratory analysis of price, sales and time patterns.
4. Define treatment, outcome, target population, confounders and identification assumptions.
5. Compare descriptive and predictive baselines with a DML estimator, if suitable.
6. Report estimates and uncertainty; run robustness checks.
7. Explore revenue/profit scenarios only with explicit assumptions.
8. Document limitations and prepare the final report and presentation.

## Candidate data
Initial candidate: [UCI Online Retail](https://archive.ics.uci.edu/dataset/352/online+retail). Inspect official documentation and terms before use. The data is transaction-level and does not automatically identify causal price effects; transaction selection and missing non-purchase opportunities are important limitations.

## Setup
Python 3.11 recommended.

```bash
python -m venv .venv
# Windows PowerShell
.venv\Scripts\Activate.ps1
# macOS/Linux
# source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
jupyter lab
```

Download data directly from the official source and keep raw data out of Git unless its terms explicitly permit redistribution. Use fixed random seeds and document package versions.

## Project status
Project foundation and methodology have been documented. The dataset has not yet been validated for causal identification, and no model performance or profit uplift is claimed.

## Research integrity
Prediction accuracy is not causal validity. DML cannot correct unobserved confounding by itself. If the available dataset does not justify causal identification, document the limitation and restrict conclusions rather than fabricate effects.
