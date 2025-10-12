Predicting the Income of NYC Residents

Author: Danny Weng
Date: March 13, 2024
Course: Statistical Computing — 36-350

Overview

New York City, home to roughly 8.5 million residents, is one of the most diverse and economically dynamic cities in the world. However, despite its cultural vibrancy, the city faces a long-standing housing affordability crisis.
This project uses data from the New York City Housing and Vacancy Survey (NYCHVS) to analyze how demographic and housing-related variables influence household income.
We apply linear regression modeling to study the effects of age, housing maintenance deficiencies, and the year of moving to NYC on income levels.

Data Description

The dataset includes information from 299 New York households.

Variables:

Income – Total household income (USD) (response variable)

Age – Age of respondent (years)

MaintenanceDef – Number of maintenance deficiencies (2002–2005)

NYCMove – Year respondent moved to New York City

Analysis Summary

Exploratory Data Analysis:

Histograms and summary statistics show right-skewed income and maintenance distributions.

Age is approximately normal; NYCMove is left-skewed.

Scatter plots indicate no strong linear patterns with income.

Modeling:

Model: Income ~ Age + MaintenanceDef + NYCMove

Checked multicollinearity using VIF (none above 2.5).

Verified regression assumptions using residual and Q-Q plots.

Model R² = 0.0298, p-value = 0.030, suggesting modest significance.

Prediction Example:
For a 53-year-old respondent with 3 maintenance deficiencies who moved to NYC in 1987,
predicted income = $39,320.23.

Findings & Discussion

The three predictors jointly explain a small but statistically significant portion of income variation.

Model assumptions are satisfied, but low R² suggests that additional variables (education, occupation, borough) could better explain income differences.

Insights from this model highlight how housing quality and residential history may relate to income inequality across NYC households.

Future Work

Add socioeconomic predictors like education level or job sector.

Explore nonlinear or interaction effects.

Evaluate predictive performance with cross-validation.

Reproducibility

Language: R
Key Packages: knitr, kableExtra, pander, readr, magrittr, car, interactions, leaps

How to run:

Clone this repository.

Open the .Rmd file in RStudio.

Install all required packages.

Knit to HTML or PDF to reproduce analysis.

License

MIT License
