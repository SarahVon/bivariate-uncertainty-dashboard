# Bivariate & Uncertainty Dashboard

A static visualization exploring relationships among crime categories and their spatial distribution across King County, Washington.

## Analysis sequence

1. **Compare crime categories.** A correlation matrix summarizes relationships among average property, society, and personal crime rates.
2. **Add uncertainty and scale.** Scatterplots add Pearson correlation values and confidence bands; point size introduces a third-variable comparison.
3. **Add spatial context.** A map shows ten-year average crime rates by King County city, using a stepped diverging color scale and larger/darker points for comparison. Labels call out the highest-rate cities while retaining all cities in the map.

## Visualization

![Bivariate crime and uncertainty dashboard](bivariate-uncertainty-dashboard.png)

*Static dashboard combining correlation views, uncertainty bands, and a county map of average crime rates.*

## Data sources and permissions

The underlying crime data were sourced from the Washington State Statistical Analysis Center (WSSAC). This repository contains the final visualization and a sanitized narrative, not the original source tables. Confirm current source terms and attribution requirements before reuse.

## Limitations

The dashboard is an exploratory summary and should not be used to infer causation. Aggregation can hide within-city variation, and crime patterns may reflect reporting practices, socioeconomic conditions, policing, and other factors not represented here. The published artifact is static, so interactive filtering is unavailable.

## Reproducibility

The original dashboard build environment and source data are not included. To reproduce or extend the work, obtain the relevant WSSAC data, document the extraction date and transformations, then recreate the correlation, uncertainty, and map views using the sequence above.
