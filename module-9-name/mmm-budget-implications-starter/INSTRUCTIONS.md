# Marketing Mix Modeling: Channel Contributions and Budget Implications

## Scenario

Following the MMM baseline, you will extract channel-level contribution signals from the model coefficients and translate them into a directional budget recommendation for the growth team. This requires both a technical output (ranked channel table and chart) and responsible framing of the MMM's limitations.

## Your task

Using the starter notebook provided in the workspace, produce:

1. A ranked channel coefficient table sorted by value
2. A horizontal bar chart of channel coefficients with a reference line at zero
3. A written directional budget recommendation

## Data

Use `marketing_weekly_channels.csv` from the `Project_Data` folder.

## Requirements

- Refit the MMM with the same setup as the baseline exercise (adstock `alpha=0.3`, `Ridge(alpha=1.0)`, time-based 80/20 split)
- Extract coefficients for adstock columns only — exclude time control columns (`t`, `sin52`, `cos52`)
- Budget recommendation must name the top 1–2 channels to prioritize by coefficient sign and magnitude
- The following sentence must appear **verbatim** in your recommendation: *"MMM results are correlational (directional), not causal."*
- Recommendation must include at least one concrete validation step before making large reallocations (e.g., holdout test, geo-split experiment)

## Deliverable

Your completed notebook with all code cells run, a channel coefficient chart, and a filled-in budget recommendation that includes the required caveat sentence and a validation step.
