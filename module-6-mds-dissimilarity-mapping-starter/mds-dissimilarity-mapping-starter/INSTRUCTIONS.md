# Building a Perceptual Map with Multidimensional Scaling (MDS)

## Scenario

A meal kit product team wants to understand how similar or different its
candidate plan configurations appear based on their feature attributes. You will
derive a dissimilarity matrix from plan characteristics, use MDS to create a 2D
perceptual map, and interpret the map to identify positioning opportunities and
cannibalization risk.

## Your task

Using the starter notebook provided in the workspace, produce:

1. A dissimilarity matrix **D** (plan × plan) derived from standardized plan
   attributes
2. A labeled 2D MDS perceptual map
3. Identification of the **closest substitute pair** (smallest off-diagonal
   distance)
4. Identification of the **whitespace opportunity** (plan with the largest
   average distance to all others)
5. A 2–4 sentence written interpretation with positioning implications

## Data

Use `mealkit_plans.csv` from the `Exercise_Data` folder.

## Data description

| Column | Description |
|---|---|
| `plan` | Plan name (QuickBite, Classic, Premium, FamilyFeast) |
| `price_per_week` | Weekly price in USD |
| `meals_per_week` | Number of meals per week |
| `servings` | Servings per meal |
| `cuisine_variety` | `standard` or `premium` |
| `dietary_options` | `no` or `yes` |
| `live_cooking_class` | `no` or `yes` |

## Requirements

- Engineer features before computing distances: `log_price = log(price_per_week)`,
  binary flags for `cuisine_variety`, `dietary_options`, `live_cooking_class`,
  plus `meals_per_week` and `servings` as numeric
- Standardize all features with `StandardScaler` before computing Euclidean
  distances
- Run `MDS(n_components=2, dissimilarity="precomputed", random_state=42)`
- Closest substitute pair must be identified programmatically from **D** (not by
  visual inspection)
- Written interpretation must reference specific plan names and numeric distances

## Deliverable

Your completed notebook with all code cells run, a labeled perceptual map, and a
filled-in positioning interpretation addressing cannibalization risk and
differentiation opportunity.
