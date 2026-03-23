# Identifying Latent Value Drivers with Factor Analysis

## Scenario

A survey captured 16 Likert-scale items (Q01–Q16) measuring customer attitudes toward various aspects of a subscription service. Many of these items likely reflect a smaller number of underlying constructs — for example, "value for money," "content quality," or "convenience." Your goal is to run exploratory factor analysis to identify these latent constructs and translate them into actionable messaging guidance.

## Your task

Using the starter notebook provided in the workspace, produce:

1. A fitted FactorAnalysis model with 3 factors
2. A loadings table (items × factors)
3. A heatmap of the loadings table
4. The top 3 items per factor by absolute loading value
5. A label/name for each factor based on its top items, plus 2–3 sentences per factor translating the top items into messaging or segmentation guidance

## Data

Use `survey_value_drivers.csv` from the `Project_Data` folder.

## Requirements

- Standardize the Likert items before fitting using `StandardScaler`
- Use `sklearn.decomposition.FactorAnalysis(n_components=3, random_state=42)`
- Loadings table must have items as rows and factors as columns, with values from `fa.components_.T`
- Factor labels must reference specific item names from the loadings table
- Written interpretation must specify which customer segment might score high on each factor and what messaging would resonate

## Deliverable

Your completed notebook with all code cells run, a loadings heatmap, and a filled-in factor interpretation section with one label and 2–3 sentences of business guidance per factor.
