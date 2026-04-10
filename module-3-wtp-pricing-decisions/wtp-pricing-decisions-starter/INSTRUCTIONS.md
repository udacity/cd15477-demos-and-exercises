# Willingness-to-Pay Estimation and Plan Pricing Decisions

## Scenario

A pricing team at a meal kit company needs to understand how much customers
would pay for specific plan features. Using part-worth utilities estimated from
conjoint choice data, you will derive directional willingness-to-pay (WTP) for
key features and score candidate plans to recommend a launch configuration.

## Your task

Using the starter notebook provided in the workspace, produce:

1. Directional WTP estimates (in USD/week) for at least **two features** using
   the coefficient ratio method
2. A scored and ranked table of all candidate plans
3. A bar chart of plan scores
4. A stated plan recommendation with pricing rationale and an
   assumptions/limitations checklist

## Data

Use `mealkit_choice_tasks.csv` and `mealkit_plans.csv` from the `Exercise_Data`
folder.

## Data description

`mealkit_plans.csv` contains four named candidate plans with the following fields:

| Column | Description |
|---|---|
| `plan` | Plan name (QuickBite, Classic, Premium, FamilyFeast) |
| `price_per_week` | Weekly plan price in USD |
| `meals_per_week` | Number of meals per week |
| `servings` | Servings per meal |
| `cuisine_variety` | `standard` or `premium` |
| `dietary_options` | `no` or `yes` |
| `live_cooking_class` | `no` or `yes` |

## Requirements

- Refit the conjoint logistic regression model from the part-worth utilities
  exercise using `mealkit_choice_tasks.csv`
- WTP formula: `WTP_feature = −β_feature / β_price`
- WTP computation must show the numeric result explicitly (e.g.,
  `WTP for Dietary Options: $X.XX/week`)
- Plan scoring uses `model.predict_proba` on features from `mealkit_plans.csv`
- Recommendation must name a specific plan and reference at least one WTP value
- Assumptions/Limitations checklist must include at least three items

## Deliverable

Your completed notebook with all code cells run, a ranked plan table, and a
filled-in recommendation section with WTP evidence and a limitations checklist.
