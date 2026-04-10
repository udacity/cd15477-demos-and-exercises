# Marketing Mix Modeling: Feature Engineering and Baseline Fit

## Scenario

A meal kit company's growth team wants to understand how weekly marketing
channel spend relates to revenue over a two-year period. Your goal is to
engineer the features needed for a time-aware marketing mix model — including
adstock/carryover features and seasonality controls — then fit a Ridge
regression and evaluate out-of-sample performance.

## Your task

Using the starter notebook provided in the workspace, produce:

1. Adstock-transformed features for all 5 marketing channels
2. Time controls: a linear trend variable `t` and weekly seasonality terms
   (`sin52`, `cos52`)
3. A Ridge regression model fit on the training period
4. Test MAE reported numerically
5. An Actual vs Predicted plot for the test period
6. A written assessment of model fit quality and trustworthiness

## Data

Use `mealkit_marketing_weekly.csv` from the `Exercise_Data` folder.

## Data description

| Column | Description |
|---|---|
| `week` | Week index (1–104, representing two years of data) |
| `weekly_revenue` | Total revenue for the week (USD) |
| `spend_search` | Search advertising spend (USD) |
| `spend_social` | Social media spend (USD) |
| `spend_influencer` | Influencer marketing spend (USD) |
| `spend_email` | Email marketing spend (USD) |
| `spend_affiliate` | Affiliate program spend (USD) |

## Requirements

- Apply adstock with `alpha=0.3` to all 5 channels: `spend_search`,
  `spend_social`, `spend_influencer`, `spend_email`, `spend_affiliate`
- Adstock formula: `adstock[t] = spend[t] + alpha × adstock[t−1]`
- Time-based train/test split: first **80%** of weeks = train, last **20%** =
  test — do not shuffle
- Use `Ridge(alpha=1.0)`
- Actual vs Predicted plot must have labeled axes and a legend
- Written assessment must reference the test MAE relative to the revenue
  distribution and comment on whether the model captures the general trend

## Deliverable

Your completed notebook with all code cells run, an Actual vs Predicted plot
for the test period, and a filled-in model fit assessment.
