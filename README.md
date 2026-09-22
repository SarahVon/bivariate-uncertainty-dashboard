# Bivariate and Uncertainty Dashboard

This **Tableau** dashboard explores relationships among property, societal, and personal crime rates in King County, Washington. It combines a compact correlation matrix with a proportional-symbol map to examine two related questions: how strongly the three crime categories are associated with one another, and how ten-year average crime rates vary geographically across King County cities.

I created the project to strengthen my skills in bivariate analysis, uncertainty visualization, multivariable encoding, and dashboard design. The finished dashboard is intended as an exploratory overview rather than an explanation of why crime rates differ between places.

## Project goals

- Compare pairwise relationships among property, societal, and personal crime rates.
- Communicate the direction and strength of each linear association.
- Show uncertainty surrounding the fitted relationships rather than presenting trend estimates as exact.
- Add a third measure to the scatterplots without creating separate, repetitive views.
- Place the statistical comparisons in geographic context using city-level averages.
- Create a focused dashboard that remains readable despite presenting several related measures.

## Dashboard

![Bivariate crime and uncertainty dashboard](bivariate-uncertainty-dashboard.png)

*Static export of the Tableau dashboard combining pairwise crime-rate comparisons, confidence bands, multivariable mark sizing, and a King County city map.*

## Data source and scope

The crime measures were obtained from the [Washington State Statistical Analysis Center (WSSAC)](https://sac.ofm.wa.gov/data) and summarized for cities in King County. WSSAC serves as a clearinghouse for Washington crime and justice data compiled from multiple agencies and reporting systems. The analysis uses three broad categories:

| Measure | Role in the dashboard |
| --- | --- |
| Property crime rate | Compared with societal and personal crime rates in the correlation views |
| Societal crime rate | Compared with property and personal crime rates in the correlation views |
| Personal crime rate | Compared with property and societal crime rates in the correlation views |
| Ten-year average crime rate | Used to compare the overall geographic pattern among King County cities |

The repository contains the final dashboard image and project documentation, but not the original WSSAC tables or row-level records. The visualization should therefore be treated as a documented personal project artifact rather than a fully packaged data release.

## Tools and methods

I built the dashboard in **Tableau**, using the following analytical and design techniques:

- Data preparation and aggregation
- Pairwise scatterplots
- Pearson correlation coefficients
- Fitted trend relationships and confidence bands
- Multivariable encoding through mark size
- Proportional-symbol mapping
- Stepped color classification
- Selective labeling and annotation
- Dashboard layout and visual hierarchy

## Dashboard design

### Pairwise correlation views

The upper portion of the dashboard uses a correlation-matrix structure to compare the three crime categories. Because a complete three-by-three matrix would repeat the same relationships and include unnecessary self-comparisons, I retained only the three unique pairings. This reduced nine possible panels to the views needed for the analysis and made the dashboard easier to scan.

Each scatterplot includes a **Pearson correlation coefficient** to summarize the direction and strength of the linear relationship. Confidence bands show the uncertainty around the fitted relationship, helping distinguish an estimated pattern from a perfectly known trend.

Point size represents the third crime category not assigned to the scatterplot axes. This adds another layer of comparison within each view and allows all three measures to contribute without requiring additional charts. Descriptive panel titles identify the measures being compared directly rather than relying only on axis labels.

### Geographic context

The map summarizes ten-year average crime rates by King County city. Larger, darker marks represent higher values, supporting quick comparison while keeping every city in view. A stepped diverging color scale separates the values into readable classes rather than implying more precision than the map can reasonably display.

The five cities with the highest mapped rates are highlighted. These annotations create a clear entry point into the map while avoiding the clutter that would result from giving every city equal visual emphasis.

## Design development

The dashboard changed substantially from its first draft. The most important revision was removing the redundant sections of the correlation matrix, which created more space for the three meaningful comparisons. I also introduced variable mark sizing, replaced generic chart names with descriptive titles, and revised the map with stepped colors and more selective annotation.

These changes improved the visual hierarchy and made the analytical structure easier to understand. They also reinforced an important part of my visualization process: adding information is only useful when the encoding remains clear, and removing repetition can be just as valuable as adding another chart.

## Interpretation

The dashboard is designed to support comparison rather than make a causal claim. The scatterplots allow viewers to assess whether two crime categories tend to rise or fall together, while the coefficients summarize those relationships and the confidence bands communicate uncertainty. The map then shows whether higher and lower ten-year averages appear concentrated in particular cities.

These views should be read together but not treated as equivalent. The scatterplots describe associations among summarized measures, while the map describes geographic variation. Neither establishes why a relationship or spatial pattern exists.

## Limitations

- Correlation measures linear association and does not establish causation.
- City-level and ten-year averages can conceal annual change and variation within cities.
- Differences may reflect population, reporting practices, missing data, classification changes, or other factors not shown in the dashboard.
- Crime patterns may also be associated with socioeconomic conditions, land use, policing, and policy differences that were outside the project's scope.
- Encoding a third variable through point size supports comparison but is less precise than a dedicated chart.
- The repository contains a static image, so viewers cannot access Tableau tooltips, filters, or underlying values.

This dashboard is best understood as an exploratory view of summarized crime data and a demonstration of analytical visualization techniques, not as a ranking of community safety or a basis for policy decisions.

## Repository contents

```text
bivariate-uncertainty-dashboard.png   Static Tableau dashboard export
project-notes.md                      Supporting project narrative
README.md                             Project overview, methods, and interpretation
```

Exact numeric reproduction would require the original WSSAC source tables, aggregation rules, and Tableau workbook. With those materials, the dashboard can be rebuilt by preparing comparable city-level measures, constructing the three unique pairwise views, adding the statistical annotations and confidence bands, and recreating the ten-year average map.
