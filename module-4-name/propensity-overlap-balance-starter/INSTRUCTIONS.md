# Propensity Modeling and Pre-Treatment Balance Diagnostics

## Scenario

A product team ran a promotional upgrade offer to a subset of users. Because offer assignment was not randomized, treated and control groups may differ on key observable characteristics. Before estimating any causal effect, you need to build a propensity model and evaluate whether a fair comparison between groups is feasible.

## Your task

Using the starter notebook provided in the workspace, produce:

1. A fitted propensity score model using the required covariates
2. A treated vs. control propensity overlap plot
3. A standardized mean difference (SMD) table for all four numeric covariates (before weighting)
4. A written assessment of overlap adequacy and covariate imbalance

## Data

Use `observational_offer_adoption.csv` from the `Project_Data` folder.

## Requirements

- Treatment variable: `offer_received`
- Numeric covariates: `age`, `tenure_days`, `prior_spend_12m`, `sessions_30d`
- Categorical covariates: `region`, `device` — must be encoded before fitting
- Report SMD for all four numeric covariates; flag any with `|SMD| > 0.1` as meaningfully imbalanced
- Overlap plot must separate treated and control distributions with labeled axes

## Deliverable

Your completed notebook with all code cells run and a filled-in assessment answering: whether overlap is adequate, which covariate is most imbalanced, and whether a propensity-adjusted analysis is feasible.
