# Propensity Modeling and Pre-Treatment Balance Diagnostics

## Scenario

A meal kit company offered a "first box free" promotion to a subset of
prospective users. Because the offer was targeted rather than randomized,
users who received it may differ systematically from those who did not.
Before estimating any causal effect, you need to build a propensity model
and evaluate whether a fair comparison between groups is feasible.

## Your task

Using the starter notebook provided in the workspace, produce:

1. A fitted propensity score model using the required covariates
2. A treated vs. control propensity overlap plot
3. A standardized mean difference (SMD) table for all four numeric covariates
   (before weighting)
4. A written assessment of overlap adequacy and covariate imbalance

## Data

Use `mealkit_trial_adoption.csv` from the `Exercise_Data` folder.

## Data description

| Column | Description |
|---|---|
| `user_id` | Unique user identifier |
| `trial_offer_sent` | 1 = received the "first box free" offer, 0 = did not |
| `converted_to_paid` | 1 = converted to a paid plan within 30 days |
| `first_month_revenue` | Revenue in the first 30 days (USD) |
| `age` | User age in years |
| `household_size` | Number of people in the household |
| `prior_orders` | Number of food delivery orders in the past 6 months |
| `weekly_app_sessions` | Average weekly app sessions in the past month |
| `region` | Geographic region (categorical: Northeast, Southeast, Midwest, West) |
| `device` | Primary device (categorical: mobile, desktop, tablet) |

## Requirements

- Treatment variable: `trial_offer_sent`
- Numeric covariates: `age`, `household_size`, `prior_orders`,
  `weekly_app_sessions`
- Categorical covariates: `region`, `device` — must be encoded before fitting
- Report SMD for all four numeric covariates; flag any with `|SMD| > 0.1` as
  meaningfully imbalanced
- Overlap plot must separate treated and control distributions with labeled axes

## Deliverable

Your completed notebook with all code cells run and a filled-in assessment
answering: whether overlap is adequate, which covariate is most imbalanced, and
whether a propensity-adjusted analysis is feasible.
