# Estimating Part-Worth Utilities from Conjoint Choice Data

## Scenario

You have choice-based conjoint survey data where prospective customers selected
their preferred meal kit plan from three alternatives across multiple tasks.
Your goal is to estimate part-worth utilities — the utility contribution of each
attribute level — and compute attribute importance to rank which plan attributes
most drive customer preference.

## Your task

Using the starter notebook provided in the workspace, produce:

1. A fitted choice model with part-worth utilities for each attribute level
2. An attribute importance table (range-scaled by attribute)
3. A horizontal bar chart of attribute importance sorted descending
4. A written answer: which attribute matters most, and what does that imply for
   plan design?

## Data

Use `mealkit_choice_tasks.csv` from the `Exercise_Data` folder.

## Data description

| Column | Description |
|---|---|
| `price_per_week` | Weekly plan price in USD (continuous) |
| `meals_per_week` | Meals included per week (2, 4, 6 — treat as continuous) |
| `servings` | Servings per meal (1, 2, 4 — treat as continuous) |
| `cuisine_variety` | Cuisine tier: `standard` or `premium` |
| `dietary_options` | Dietary accommodation: `no` or `yes` |
| `live_cooking_class` | Weekly live class included: `no` or `yes` |
| `chosen` | 1 = chosen, 0 = not chosen |

## Requirements

- Treat `price_per_week`, `meals_per_week`, `servings` as continuous features
- Encode `cuisine_variety`, `dietary_options`, `live_cooking_class` as dummies;
  drop reference levels: `cuisine_variety_standard`, `dietary_options_no`,
  `live_cooking_class_no`
- Attribute importance for continuous features = `|coefficient| × (max − min
  observed value)`
- Attribute importance for binary/dummy features = `|coefficient|`
- Reflection must reference specific importance values from your table

## Deliverable

Your completed notebook with all code cells run and a filled-in reflection
answering which attribute has the highest importance, which has the lowest, and
which single attribute you would recommend improving for the new plan tier.
