# Willingness-to-Pay Estimation and Bundle Pricing Decisions

## Scenario

A pricing team needs to understand how much customers would pay for specific subscription features. Using part-worth utilities estimated from conjoint choice data, you will derive directional willingness-to-pay (WTP) for key features and score candidate bundles to recommend a launch configuration.

## Your task

Using the starter notebook provided in the workspace, produce:

1. Directional WTP estimates (in USD/month) for at least **two features** using the coefficient ratio method
2. A scored and ranked table of all candidate bundles
3. A bar chart of bundle scores
4. A stated bundle recommendation with pricing rationale and an assumptions/limitations checklist

## Data

Use `choice_conjoint_tasks.csv` and `candidate_bundles.csv` from the `Project_Data` folder.

## Requirements

- Refit the conjoint logistic regression model from the part-worth utilities exercise
- WTP formula: `WTP_feature = −β_feature / β_price`
- WTP computation must show the numeric result explicitly (e.g., `WTP for No Ads: $X.XX/month`)
- Bundle scoring uses `model.predict_proba` on features from `candidate_bundles.csv`
- Recommendation must name a specific bundle and reference at least one WTP value
- Assumptions/Limitations checklist must include at least three items

## Deliverable

Your completed notebook with all code cells run, a ranked bundle table, and a filled-in recommendation section with WTP evidence and a limitations checklist.
