# Analysis prompt

## Prompt issued 2026-10-18

> Grab the question you think is best and run the analysis. Do not ask to confirm before proceeding on the analysis, just pick the question and go.

## Question selected by Codex

Among houses with the same above-ground living area, how do expected sale prices differ across Ames neighborhoods?

## Planned method

Fit an ordinary least squares model with neighborhood fixed intercepts and a shared linear term for above-ground living area. Compare estimated neighborhood sale prices at the dataset-wide mean living area. Treat the results as descriptive and report limitations.
