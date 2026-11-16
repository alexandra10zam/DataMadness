# Data Madness: Drug Overdose Deaths in the USA (1999-2021)

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![statsmodels](https://img.shields.io/badge/statsmodels-time%20series-4051B5)

A **team data-analysis project** (Maastricht University) on two decades of US drug-overdose mortality data published by the NIH and mirrored on Kaggle. Before the analysis, the team checked that the two sources contained identical data.

## Research questions

1. Which categories of drugs cause the most overdose deaths, broken down by age group?
2. Did the COVID-19 pandemic increase overdose deaths?
3. Demographics: how do deaths differ by sex and ethnicity, and which sex uses a wider variety of drug types?

## What's inside

| Step | Techniques |
|---|---|
| **Data cleaning** | Missing-value profiling, dropping columns with more than 30% missing values, reshaping wide tables into tidy format |
| **Time-series analysis** | Stationarity check (ADF test), ACF/PACF, **ARIMA(1,1,1)** fitted on the pre-2020 years, to compare the actual pandemic-era deaths with the pre-COVID trend |
| **Clustering** | **K-Means** (elbow method, one-hot encoded + scaled features) on death counts by ethnicity and by sex |
| **Classification** | Logistic Regression that separates high-risk from low-risk years (above or below the median death count) |
| **Ethics** | Source verification and a discussion of how the data is used |

## Run it

```bash
pip install pandas numpy scikit-learn statsmodels matplotlib seaborn openpyxl jupyter
jupyter notebook Data-madness.ipynb
```

Data files: `Overdose1999-2021.xlsx`, `Count_by_demo.xlsx`.
