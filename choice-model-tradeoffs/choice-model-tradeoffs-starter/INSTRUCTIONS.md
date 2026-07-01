# Modeling Customer Trade-offs with a Choice Model

## Scenario

A meal kit delivery company surveyed prospective customers on subscription plan
preferences. Each respondent chose among three plan alternatives across eight
tasks. Your goal is to fit a choice model, identify which plan features drive
selection, and build a price sensitivity chart to support product decisions.

## Your task

Using the starter notebook provided in the workspace, produce:

1. A fitted logistic regression (choice model) with interpretable coefficients
2. A coefficient plot showing feature importance by absolute magnitude
3. A price sensitivity chart (average choose-rate by price level)
4. A markdown list of the **top 3 feature drivers** with directional interpretation

## Data

Use `mealkit_choice_tasks.csv` from the `Exercise_Data` folder.

## Data description

Each row represents one alternative shown to one respondent in one task.

| Column | Description |
|---|---|
| `respondent_id` | Unique respondent identifier |
| `task_id` | Task number (1–8 per respondent) |
| `alternative` | Alternative label within task (A, B, C) |
| `chosen` | 1 = chosen, 0 = not chosen |
| `price_per_week` | Weekly plan price in USD (continuous) |
| `meals_per_week` | Number of meals per week (2, 4, 6) |
| `servings` | Servings per meal (1, 2, 4) |
| `cuisine_variety` | Cuisine tier: `standard` or `premium` |
| `dietary_options` | Dietary accommodation: `no` or `yes` |
| `live_cooking_class` | Weekly live class included: `no` or `yes` |

## Requirements

- Encode categorical features (`cuisine_variety`, `dietary_options`,
  `live_cooking_class`) before fitting
- Model outcome: `chosen` column (1 = chosen, 0 = not chosen)
- Drop reference levels: `cuisine_variety_standard`, `dietary_options_no`,
  `live_cooking_class_no`
- Identify the top 3 drivers by **absolute coefficient magnitude** and state
  each driver's direction
- Price sensitivity chart must have labeled axes

## Deliverable

Your completed notebook with all code cells run and a filled-in reflection
section identifying the top 3 drivers and their product decision implications.
