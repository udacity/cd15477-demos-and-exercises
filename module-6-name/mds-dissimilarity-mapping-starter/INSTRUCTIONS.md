# Building a Perceptual Map with Multidimensional Scaling (MDS)

## Scenario

A product team wants to understand how similar or different its subscription bundles appear based on their feature attributes. You will derive a dissimilarity matrix from bundle characteristics, use MDS to create a 2D perceptual map, and interpret the map to identify positioning opportunities and cannibalization risk.

## Your task

Using the starter notebook provided in the workspace, produce:

1. A dissimilarity matrix **D** (bundle × bundle) derived from standardized bundle attributes
2. A labeled 2D MDS perceptual map
3. Identification of the **closest substitute pair** (smallest off-diagonal distance)
4. Identification of the **whitespace opportunity** (bundle with the largest average distance to all others)
5. A 2–4 sentence written interpretation with positioning implications

## Data

Use `candidate_bundles.csv` from the `Project_Data` folder.

## Requirements

- Engineer features before computing distances: `log_storage = log(storage_gb)`, binary flags for `support`, `ads`, `offline_download`, plus `price_usd` and `family_seats`
- Standardize all features with `StandardScaler` before computing Euclidean distances
- Run `MDS(n_components=2, dissimilarity="precomputed", random_state=42)`
- Closest substitute pair must be identified programmatically from `D` (not by visual inspection)
- Written interpretation must reference specific bundle names and numeric distances

## Deliverable

Your completed notebook with all code cells run, a labeled perceptual map, and a filled-in positioning interpretation addressing cannibalization risk and differentiation opportunity.
