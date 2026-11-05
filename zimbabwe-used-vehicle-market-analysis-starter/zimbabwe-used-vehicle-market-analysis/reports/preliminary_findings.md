# Preliminary Findings and Interpretation

## Snapshot
The starter dataset contains 21 public listing observations collected on 5 November 2026:
- 18 Toyota Axio listings from two listing portals.
- 1 Honda Fit, 1 Nissan X-Trail and 1 Toyota Fortuner from a Harare marketplace results page.
- All observed asking prices are shown in USD.

## What can and cannot be concluded
This dataset is suitable for demonstrating data preparation and exploratory analysis. It is **not** sufficient to estimate Zimbabwe-wide used-car prices or infer causal effects. It is strongly concentrated in one model (Toyota Axio), uses convenience sampling, and may include cross-platform duplicate advertisements.

## Next data-quality tasks
1. Verify whether listings are still live.
2. Check for cross-platform duplicates using make, model, year, price and mileage.
3. Capture individual advert URLs where available.
4. Expand the sample across at least 8–10 makes and several body types.
5. Record whether prices are negotiable, before duty, or duty paid.
6. Keep missing transmission/fuel fields blank until verified.

## Analysis note
The notebook calculates descriptive statistics and creates charts from the available observations. Any averages or correlations should be described as sample-level summaries only.
