# Bivariate & Uncertainty Dashboard

A static visualization of relationships among property, societal, and personal crime rates and their spatial distribution across King County, Washington.

## Purpose

I created this dashboard to compare pairwise crime-rate associations, show uncertainty around those comparisons, and place ten-year average rates in geographic context.

## Data boundary

The measures come from the Washington State Statistical Analysis Center (WSSAC). This repository includes the final visualization and a sanitized narrative, not the original tables, row-level records, extraction code, or dashboard build environment.

## Workflow

1. Prepare comparable average crime-rate measures.
2. Calculate pairwise Pearson correlations.
3. Add scatterplots with correlation values and confidence bands.
4. Use point size for a third-variable comparison.
5. Aggregate ten-year averages by King County city.
6. Apply a stepped diverging scale and label the five highest-rate cities while retaining all cities.

![Bivariate crime and uncertainty dashboard](bivariate-uncertainty-dashboard.png)

*Static dashboard combining correlation views, uncertainty bands, and a county map.*

## Interpretation and limitations

Correlation describes linear association in summarized data; it does not establish causation. City averages can conceal within-city variation, missingness, and reporting changes. Crime patterns may also reflect factors not represented here. The static artifact does not provide interactive filtering or underlying values.

## Reproducibility

Obtain the relevant WSSAC data under current terms, document the extraction and aggregation choices, then rebuild the correlation matrix, Pearson-*r* and confidence-band views, and city map. Exact numeric recreation is bounded by the unavailable source tables and build environment.

## Repository contents

- `bivariate-uncertainty-dashboard.png`
- `project-notes.md`
- `README.md`
