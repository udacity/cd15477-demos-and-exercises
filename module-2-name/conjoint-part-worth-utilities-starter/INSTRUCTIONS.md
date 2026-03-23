# Estimating Part-Worth Utilities from Conjoint Choice Data

## Scenario

You have choice-based conjoint survey data where customers selected their preferred subscription bundle from three alternatives across multiple tasks. Your goal is to estimate part-worth utilities — the utility contribution of each attribute level — and compute attribute importance to rank which attributes most drive customer preference.

## Your task

Using the starter notebook provided in the workspace, produce:

1. A fitted choice model with part-worth utilities for each attribute level
2. An attribute importance table (range-scaled by attribute)
3. A horizontal bar chart of attribute importance sorted descending
4. A written answer: which attribute matters most, and what does that imply for product design?

## Data

Use `choice_conjoint_tasks.csv` from the `Project_Data` folder.

## Requirements

- Treat `price_usd`, `storage_gb`, `family_seats` as continuous features
- Encode `support`, `ads`, `offline_download` as dummies; drop reference levels: `support_Standard`, `ads_Ads`, `offline_download_No`
- Attribute importance for continuous features = `|coefficient| × (max − min observed value)`
- Attribute importance for binary/dummy features = `|coefficient|`
- Reflection must reference specific importance values from your table

## Deliverable

Your completed notebook with all code cells run and a filled-in reflection answering which attribute has the highest importance, which has the lowest, and which single attribute you would recommend improving for the new tier.
