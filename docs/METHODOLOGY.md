# Methodology and Identification Notes

## Research question
Can public retail observations support an estimate of the effect of price on demand after controlling for observed confounding factors?

## Partially linear DML framework
A starting model is \(Y = \theta T + g(X) + \epsilon\), with price treatment \(T = m(X) + V\). Here \(Y\) is demand, \(X\) are observed covariates, and \(\theta\) is the target effect. DML learns nuisance functions and uses an orthogonal score with cross-fitting.

## Decisions to document before estimation
- Unit of observation and target population.
- Treatment scale (price or log-price) and outcome (quantity or a documented transformation).
- Which covariates are pre-treatment confounders and why.
- Within-product price variation and treatment overlap.
- Handling of time dependence, product identity, missing values and outliers.
- Learners, cross-fitting folds, random seeds and inference procedure.

## Identification risks
DML does not solve unobserved confounding or selection bias. UCI Online Retail records transactions, not every opportunity to buy or periods with zero sales. Observed price may be correlated with product mix, popularity, customer selection, stock availability and seller decisions. Causal identification must be justified rather than assumed.

If the dataset cannot support identification, treat its analysis as descriptive/predictive and say so plainly. A model coefficient alone does not prove that an intervention will increase sales or profit.

## Evaluation
- Predictive metrics such as held-out MAE/RMSE for prediction tasks.
- Causal estimate, standard error and confidence interval with assumptions stated.
- Uncontrolled association versus adjusted estimate and alternate specifications.
- Sensitivity to modelling choices and data restrictions.
- Pricing scenarios that disclose unit-cost assumptions; no realized uplift claim without valid evaluation.

## References
- DoubleML: https://docs.doubleml.org/
- EconML: https://econml.azurewebsites.net/
- UCI Online Retail: https://archive.ics.uci.edu/dataset/352/online+retail
