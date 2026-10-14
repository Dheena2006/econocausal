# EconoCausal Project Plan

**Cadence:** one small, reviewable milestone per day; planned daily update at 9:00 PM India Standard Time (Asia/Kolkata). The schedule is a working plan and can be compressed or extended based on dataset suitability.

| Day | Milestone | Deliverable / exit criterion |
|---|---|---|
| 1 | Research framing and repository setup | Research question, hypotheses, DML explanation, project structure, Git baseline |
| 2 | Dataset documentation | Source/licence notes, field dictionary, download instructions, reproducibility checklist |
| 3 | Data acquisition | Reproducible download/load path; raw files ignored by Git |
| 4 | Data quality audit | Shape, schema, missingness, duplicates, types, invalid values |
| 5 | EDA I | Quantity/price distributions, time coverage, returns/cancellations, documented exclusions |
| 6 | EDA II and panel feasibility | Product-time coverage, zero-sale limitation, treatment variation and support audit |
| 7 | Estimand and identification review | Define unit, treatment, outcome, controls, target population, assumptions, go/no-go decision |
| 8 | Preprocessing pipeline | Tested transformations with explicit exclusions and audit counts |
| 9 | Baseline descriptive analysis | Unadjusted price-demand relationship; explicitly labelled non-causal |
| 10 | Predictive baseline | Leakage-aware split and MAE/RMSE as predictive—not causal—metrics |
| 11 | DML implementation | PLR DML estimator, nuisance learners, cross-fitting and fixed seeds |
| 12 | Inference and diagnostics | Effect, SE, 95% CI, overlap/variation checks, warnings |
| 13 | Robustness | Alternative learners/specifications and sensitivity to control choices |
| 14 | Pricing economics | Candidate-price scenarios only if supported; cost assumptions and constraints stated |
| 15 | Evaluation summary | Baseline comparison, limitations, reproducibility run-through |
| 16 | Documentation | Methodology and results report with no unsupported claims |
| 17 | Final notebook polish | Restart-and-run-all validation; clear output and deterministic settings |
| 18 | Presentation | Internship PPT outline and visual summaries from actual results |
| 19 | Final review | Code review, dependency/licence check, secret scan, README review |
| 20 | Final delivery | Tagged project state, final progress update, known limitations and future work |

## Daily update protocol (9 PM IST)
1. Read the current progress log and inspect the repository state.
2. Complete only the next incomplete milestone—do not dump the whole project in one commit.
3. Run the relevant validation/test and document what ran or could not run.
4. Commit a focused increment with a descriptive message.
5. Append the date, files changed, checks, findings, blockers, and next step to `docs/PROGRESS.md`.
6. If GitHub connectivity or permissions prevent a push, report the blocker; never claim a push occurred when it did not.

## Gatekeeping decisions
- Do not fit a causal model until the treatment, outcome, confounders, and estimand are explicit.
- If the dataset lacks meaningful price variation or lacks a defensible set of controls/outcome opportunities, record the no-go decision or choose a more suitable public dataset.
- DML reduces certain nuisance-model regularization biases; it does not solve unobserved confounding or guarantee causal identification.
- Pricing recommendations require a credible demand response, observed/assumed unit cost, feasible price support, and clear business constraints.
