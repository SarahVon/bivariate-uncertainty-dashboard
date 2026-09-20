# Bivariate & Uncertainty Dashboard

A static visualization exploring relationships among crime categories and their spatial distribution across King County, Washington.

## Contents

- [Purpose and questions](#purpose-and-questions)
- [Variables and source boundary](#variables-and-source-boundary)
- [Workflow](#workflow)
- [Visualization sequence](#visualization-sequence)
- [Interpretation](#interpretation)
- [Limitations](#limitations)
- [Reproducibility](#reproducibility)
- [Repository contents](#repository-contents)

## Purpose and questions

The dashboard asks how average property, societal, and personal crime rates relate to one another, and how ten-year average rates vary across King County cities. It is an exploratory comparison, not a causal or predictive model.

## Variables and source boundary

The displayed variables are average property, society, and personal crime rates. The underlying data were sourced from the Washington State Statistical Analysis Center (WSSAC). This repository contains the final visualization and a sanitized narrative, not the original tables, row-level records, or dashboard build environment.

## Workflow

1. Prepare comparable average crime-rate measures.
2. Calculate pairwise Pearson correlations for the category comparisons.
3. Add scatterplots with correlation values and confidence bands to show association and uncertainty.
4. Use point size to introduce a third-variable comparison in the bivariate views.
5. Aggregate ten-year average rates by King County city for the spatial view.
6. Apply a stepped diverging color scale, larger/darker points, and labels for the five highest-rate cities while retaining all cities.

## Visualization sequence

### Correlation and uncertainty

The correlation matrix establishes the relationships among the three categories. Scatterplots then show the paired observations, Pearson’s *r*, confidence bands, and an additional size encoding.

### Spatial comparison

![Bivariate crime and uncertainty dashboard](bivariate-uncertainty-dashboard.png)

*Static dashboard combining correlation views, uncertainty bands, and a county map of average crime rates.*

The map adds geographic context to the category comparisons and emphasizes the highest-rate cities without removing the rest of the study area.

## Interpretation

The artifact supports comparison of association, uncertainty, and geographic pattern. Correlation values describe linear association in the summarized data; they do not establish that one crime category causes another. City-level patterns describe averages and should not be read as within-city conditions.

## Limitations

Aggregation can hide within-city variation, missingness, and changes in reporting practices. Crime patterns may also reflect socioeconomic conditions, policing, and other factors not represented here. The published artifact is static, so interactive filtering and underlying values are unavailable.

## Reproducibility

The original source tables, extraction date, transformation code, and dashboard environment are not published. Reproduction requires obtaining the relevant WSSAC data under current terms, documenting the extraction and aggregation choices, then rebuilding the correlation matrix, Pearson *r* and confidence-band views, and city map. Exact numeric recreation is therefore bounded by those unavailable inputs.

## Repository contents

- `bivariate-uncertainty-dashboard.png` — static dashboard export
- `project-notes.md` — concise provenance and design notes
- `README.md` — methods, interpretation, and reproducibility boundary
