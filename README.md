# Ames Housing Neighborhood Analysis

## Analytical question

Among houses with the same above-ground living area, how do expected sale prices differ across Ames neighborhoods?

## Codex session date

October 18, 2026

## Findings

Using 2,930 sales across 28 neighborhoods, I fit a linear model with a separate neighborhood intercept and a shared linear relationship between above-ground living area and sale price. At the dataset-wide mean living area of about 1,500 square feet, adjusted expected sale prices range from about $124,500 in SWISU to $289,500 in StoneBr. The estimated association is $77.30 per additional square foot; the model R-squared is 0.745 and its RMSE is about $40,322. These are descriptive estimates, not causal effects: the model does not adjust for other property characteristics, and the estimate for GrnHill is based on only two sales.

## Run the analysis

Open [`analysis/notebooks/ames_housing_exploration.ipynb`](analysis/notebooks/ames_housing_exploration.ipynb) in VS Code, select the **Ames Week 7** kernel, and run the cells from top to bottom. The notebook reads `AmesHousing-1.csv` from the repository root and writes the summary table and chart to `analysis/outputs/`.

## Analysis artifacts

- [`analysis/outputs/tables/neighborhood_adjusted_summary.csv`](analysis/outputs/tables/neighborhood_adjusted_summary.csv) — neighborhood counts, unadjusted medians, and model-adjusted estimates.
- [`analysis/outputs/figures/neighborhood_adjusted_prices.png`](analysis/outputs/figures/neighborhood_adjusted_prices.png) — observed neighborhood medians compared with prices adjusted for living area.
- [`prompts/01_final_analysis.md`](prompts/01_final_analysis.md) — selected analytical prompt and method.
- [`log/ai-workflow-log.md`](log/ai-workflow-log.md) — accepted, modified, and rejected work with rationale.
