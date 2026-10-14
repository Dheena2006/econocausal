# Methodology and Decision Log

## Target estimand (provisional)
A partially linear regression (PLR) DML parameter for the effect of a defined price treatment on a defined demand outcome, conditional on a specified set of observed covariates. Final variables and scale will be selected only after dataset inspection.

## Working model
Y = theta * T + g(X) + epsilon
T = m(X) + V

DML estimates nuisance functions for the outcome and treatment, uses cross-fitting and an orthogonal score, and provides inference for theta under its assumptions.

## Identification assumptions to assess
- Conditional exchangeability/no important unobserved confounding given X.
- Treatment variation/overlap (prices vary sufficiently across comparable observations).
- Correctly defined unit and outcome; sampling/selection mechanism understood.
- No problematic interference, anticipation, or uncontrolled time/product shocks for the proposed estimand.
- Nuisance models and inference procedure appropriate for dependence structure.

These assumptions cannot be proven from data alone. The report will discuss evidence and limitations.

## Important distinction
Predictive MAE/RMSE evaluate prediction. They do not validate a causal estimate. A confidence interval quantifies estimator uncertainty under the model and inference assumptions; it does not account for all unobserved confounding automatically.

## Pricing decisions
Only considered after causal/demand estimates and support diagnostics. State unit-cost assumptions; report revenue and profit separately; restrict candidates to observed/supportable price ranges and avoid extrapolation.
