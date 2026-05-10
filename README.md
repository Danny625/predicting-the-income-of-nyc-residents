# 🏙️ Predicting NYC Household Income

A small regression analysis project using New York City housing survey data.

I used a sample of NYC households to explore whether age, housing maintenance deficiencies, and year moved to New York City can help explain household income. The project is written in R Markdown and focuses on exploratory analysis, linear regression, model diagnostics, and interpretation.

## 🛠 Tools

- R
- R Markdown
- tidyverse / readr
- car
- kableExtra
- linear regression
- model diagnostics

## ✨ What it analyzes

### Household income

The response variable is total household income. The analysis looks at how income varies across the sample and whether it can be explained by housing and demographic variables.

### Predictor variables

The model uses:

- respondent age
- number of housing maintenance deficiencies
- year the respondent moved to NYC

### Regression modeling

I fit and compared several linear regression models, then checked assumptions using residual plots, Q-Q plots, and VIF values for multicollinearity.

The final model using all three predictors had the highest R-squared value among the models tested, but the overall predictive power was still low. That was one of the main takeaways: the variables are related to income, but they do not explain most of the variation.

## 🚦 How to run

### 1. Clone the repo

```bash
git clone https://github.com/Danny625/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
```

### 2. Install packages

Open R or RStudio and run:

```r
install.packages(c(
  "knitr",
  "kableExtra",
  "pander",
  "readr",
  "magrittr",
  "car",
  "interactions",
  "leaps"
))
```

### 3. Add the data

Make sure the dataset is in the project folder:

```text
nyc.csv
```

### 4. Knit the report

Open the `.Rmd` file in RStudio and click **Knit**, or run:

```r
rmarkdown::render("YOUR_FILE_NAME.Rmd")
```

## 📁 Project files

```text
.
├── README.md
├── NYCHousing.pdf          # Rendered report
├── YOUR_FILE_NAME.Rmd      # Main analysis file
└── nyc.csv                 # NYC housing survey sample
```

## 🤖 How it works

The analysis starts by exploring the distributions of income, age, maintenance deficiencies, and year moved to NYC. Then it checks the relationships between income and each predictor using scatter plots.

After that, I fit a multiple linear regression model, checked for multicollinearity with VIF, reviewed residual diagnostics, compared smaller models, and used the final model to make an example income prediction.

## 📌 Main takeaways

- Income in the sample is right-skewed and bimodal.
- The predictors do not show strong linear relationships with income on their own.
- Maintenance deficiencies had the clearest individual signal in the regression output.
- The full model was statistically significant, but the R-squared was low.
- More variables like education, occupation, borough, or neighborhood would likely improve prediction.

## 👤 Author

Danny Weng
