# Modeling Customer Trade-offs with a Choice Model

## Scenario

A product team surveyed customers on subscription bundle preferences. Each respondent chose among three alternatives across multiple tasks. Your goal is to fit a choice model, identify which features drive selection, and build a price sensitivity chart to support product decisions.

## Your task

Using the starter notebook provided in the workspace, produce:

1. A fitted logistic regression (choice model) with interpretable coefficients
2. A coefficient plot showing feature importance by absolute magnitude
3. A price sensitivity chart (average choose-rate by price level)
4. A markdown list of the **top 3 feature drivers** with directional interpretation

## Data

Use `choice_conjoint_tasks.csv` from the `Project_Data` folder.

## Requirements

- Encode categorical features (`support`, `ads`, `offline_download`) before fitting
- Model outcome: `chosen` column (1 = chosen, 0 = not chosen)
- Drop reference levels: `support_Standard`, `ads_Ads`, `offline_download_No`
- Identify the top 3 drivers by **absolute coefficient magnitude** and state each driver's direction
- Price sensitivity chart must have labeled axes

## Deliverable

Your completed notebook with all code cells run and a filled-in reflection section identifying the top 3 drivers and their product decision implications.
