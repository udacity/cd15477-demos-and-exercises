# IPW Effect Estimation and Post-Weighting Balance

## Scenario

Following the propensity modeling step, you will apply inverse probability
weighting (IPW) to estimate the effect of the "first box free" offer on user
conversion and first-month revenue. You will also verify that IPW successfully
reduces covariate imbalance, and compare adjusted estimates to naive
(unadjusted) estimates to quantify the impact of selection bias.

## Your task

Using the starter notebook provided in the workspace, produce:

1. IPW weights computed from propensity scores
2. An SMD table comparing covariate balance **before and after** IPW weighting
3. IPW Average Treatment Effect (ATE) for **both** `converted_to_paid` and
   `first_month_revenue`
4. Naive ATE (simple mean difference) for both outcomes, for comparison
5. A written justification for which estimate is more credible and why

## Data

Use `mealkit_trial_adoption.csv` from the `Exercise_Data` folder.

## Data description

| Column | Description |
|---|---|
| `trial_offer_sent` | Treatment indicator (1 = received offer) |
| `converted_to_paid` | Outcome 1: converted to a paid plan within 30 days |
| `first_month_revenue` | Outcome 2: revenue in the first 30 days (USD) |
| `age` | User age in years |
| `household_size` | Number of people in the household |
| `prior_orders` | Food delivery orders in the past 6 months |
| `weekly_app_sessions` | Average weekly app sessions in the past month |
| `region` | Geographic region (categorical) |
| `device` | Primary device (categorical) |

## Requirements

- Refit the propensity model with the same covariates as the previous exercise
- IPW weights: treated units = `1 / propensity`, control units =
  `1 / (1 − propensity)`
- Report both naive and IPW ATE for **both** outcomes (4 numbers total)
- Written comparison must reference specific SMD before/after values and the
  ATE difference
- The remaining unconfoundedness assumption must be acknowledged in your written
  answer

## Deliverable

Your completed notebook with all code cells run and a filled-in credibility
assessment referencing the SMD improvement and the difference between naive and
IPW estimates.
