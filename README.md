# Simple Linear Regression — Marketing ROI Analysis

A complete data science project that analyses marketing spend data across TV, Radio, and Social Media channels to identify the strongest driver of Sales using Ordinary Least Squares (OLS) regression.

---

## Project Overview

**Goal:** Determine which marketing channel yields the highest return on investment (ROI) by building a statistically valid Simple Linear Regression model and interpreting the results for business decision-making.

**Method:** Ordinary Least Squares (OLS) regression via `statsmodels`

**Dataset:** `marketing_data.csv` — 4572  observations of marketing spend (TV, Radio, Social Media) and corresponding Sales figures

---

## What This Project Covers

| Step | Description |
|------|-------------|
| Data Loading & Exploration | Load the dataset, inspect structure, check data types and statistics |
| Missing Value Handling | Identify and remove missing rows; justify the approach |
| Exploratory Data Analysis | Distribution plots, scatter plots, Pearson correlation matrix |
| Variable Selection | Rank channels by correlation with Sales; justify choice of TV |
| OLS Model Building | Fit regression using `statsmodels`, add intercept via `sm.add_constant` |
| Model Interpretation | Explain R², coefficients, p-values, and 95% confidence intervals |
| Assumption Diagnostics | Residuals vs. Fitted, Q-Q plot, Scale-Location, Breusch-Pagan test |
| Business Recommendation | Translate statistical output into plain-language ROI guidance |

---

## Project Structure

```
regression-roi/
├── regression_analysis.ipynb   # Main Jupyter Notebook (all cells executed)
├── marketing_data.csv          # Marketing spend dataset
├── README.md                   # This file
├── fig_distributions.png       # Histogram output
├── fig_scatter_channels.png    # Scatter plots output
├── fig_correlation_heatmap.png # Correlation heatmap output
├── fig_regression_line.png     # Regression line with confidence band
└── fig_diagnostics.png         # 2x2 diagnostic plots
```

---

## Environment Setup

### Requirements

- Python 3.8 or higher
- pip

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn statsmodels scipy
```

Or install all at once from the included requirements list:

```bash
pip install pandas numpy matplotlib seaborn statsmodels scipy jupyter
```

### Run the Notebook

```bash
jupyter notebook regression_analysis.ipynb
```

Or use JupyterLab:

```bash
pip install jupyterlab
jupyter lab regression_analysis.ipynb
```

---

## Key Findings (Summary)

- **TV** advertising has the highest Pearson correlation with Sales among the three channels
- The OLS model `Sales = β₀ + β₁ × TV` is statistically significant (p < 0.05)
- R-squared confirms that TV spend explains a meaningful portion of variance in Sales
- For every $1,000 increase in TV advertising spend, Sales are expected to increase by approximately β₁ × 1,000 units (see notebook output)
- **Recommendation:** Prioritise TV budget allocation; investigate Radio further via multiple regression

---

## Regression Assumptions Tested

| Assumption | Method | Result |
|------------|--------|--------|
| Linearity | Residuals vs. Fitted + LOWESS | Verified visually |
| Normality of residuals | Shapiro-Wilk test + Q-Q plot | See notebook output |
| Homoscedasticity | Breusch-Pagan test + Scale-Location | See notebook output |
| Independence | Study design (cross-sectional) | Assumed |

---

## Dependencies & Versions

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading and manipulation |
| `numpy` | Numerical operations |
| `matplotlib` | Base plotting |
| `seaborn` | Statistical visualisations |
| `statsmodels` | OLS regression, Breusch-Pagan test |
| `scipy` | Shapiro-Wilk normality test, Pearson correlation |

Run the final cell in the notebook to print exact versions used in this analysis.

---

## Author

**Olaniyi** — Data & Business Intelligence Analyst  
*National Health Fellow, Federal Ministry of Health and Social Welfare, Nigeria*

---

## License

This project is submitted as part of a structured data science learning programme. Dataset and code are for educational purposes.
