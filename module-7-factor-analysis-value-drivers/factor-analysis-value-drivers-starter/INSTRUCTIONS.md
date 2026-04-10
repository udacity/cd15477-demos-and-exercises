# Identifying Latent Value Drivers with Factor Analysis

## Scenario

A meal kit company surveyed 800 customers using 16 Likert-scale items
measuring attitudes toward cooking habits, health preferences, convenience,
and budget sensitivity. Many of these items likely reflect a smaller number
of underlying constructs. Your goal is to run exploratory factor analysis to
identify these latent constructs and translate them into actionable messaging
and segmentation guidance.

## Your task

Using the starter notebook provided in the workspace, produce:

1. A fitted FactorAnalysis model with 3 factors
2. A loadings table (items × factors)
3. A heatmap of the loadings table
4. The top 3 items per factor by absolute loading value
5. A label/name for each factor based on its top items, plus 2–3 sentences per
   factor translating the top items into messaging or segmentation guidance

## Data

Use `mealkit_survey.csv` from the `Exercise_Data` folder.

## Data description

The dataset contains 800 rows (one per respondent). Survey items are scored
1–5 (strongly disagree to strongly agree):

| Items | Broad theme |
|---|---|
| Q01–Q04 | Recipe quality and variety (higher mean ~3.6–4.0) |
| Q05–Q08 | Convenience and ease-of-preparation (moderate mean ~2.9–3.4) |
| Q09–Q12 | Value for money and budget sensitivity (lower mean ~2.3–2.6) |
| Q13–Q16 | Overall satisfaction — cross-load across all three factors |

## Requirements

- Standardize items Q01–Q16 before fitting using `StandardScaler`
- Use `sklearn.decomposition.FactorAnalysis(n_components=3, random_state=42)`
- Loadings table must have items as rows and factors as columns, with values
  from `fa.components_.T`
- Factor labels must reference specific item names from the loadings table
- Written interpretation must specify which customer segment might score high on
  each factor and what messaging would resonate

## Deliverable

Your completed notebook with all code cells run, a loadings heatmap, and a
filled-in factor interpretation section with one label and 2–3 sentences of
business guidance per factor.
