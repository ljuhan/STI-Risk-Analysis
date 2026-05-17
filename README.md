# STI Risk Analysis

## Overview
A quantitative analysis of Singapore's Straits Times Index (STI) constituents, covering the full pipeline from data ingestion through statistical modelling and strategy evaluation. The project applies financial econometrics — return distributions, hypothesis testing, and regression — to real market data from Singapore blue-chip equities.

## Repository Structure
```
analysis/       notebooks covering each stage of the analysis
data/           raw CSV files (individual stocks + global indices)
```

## Analysis Notebooks

### Data & Exploration
- **Import data** — fetches and cleans historical price data using `yfinance`
- **DataFrame** — time-series manipulation and feature inspection
- **Create new features and columns in DataFrame** — engineering log returns, rolling metrics, and derived signals

### Return Modelling
- **Models of Stock Return** — normal vs. empirical return distributions; fat-tail diagnostics
- **Frequency and Distribution** — histogram analysis of return frequencies across STI constituents
- **Outcomes and Random Variables** — probability foundations applied to equity returns

### Statistical Inference
- **Population and Sample** — sampling theory in the context of financial time series
- **Variation of Sample** — standard error, bootstrap estimation
- **Confidence Interval** — constructing CIs for mean returns and volatility estimates
- **Hypothesis testing** — t-tests and p-values applied to STI return data

### Regression & Strategy
- **Association between two random variables** — covariance and Pearson correlation between STI constituents
- **Simple linear regression model** — beta estimation against the STI index
- **Multiple linear regression model** — multi-factor return model using global indices
- **Diagnostic of models** — residual analysis, heteroscedasticity, and model fit
- **Evaluating strategy built from Regression model** — backtesting a signal derived from the regression output; risk-adjusted performance metrics

### Trading Strategy
- **Build a simple trading strategy** — moving-average crossover strategy applied to STI data with P&L analysis

## Tech Stack
- **Python 3.10+**
- **Pandas / NumPy** — time-series manipulation and vectorised financial calculations
- **Matplotlib / Seaborn** — visualisation (return distributions, heatmaps, equity curves)
- **Statsmodels** — OLS regression and diagnostics
- **yfinance** — market data retrieval

## Getting Started
```bash
pip install pandas numpy matplotlib seaborn yfinance statsmodels
jupyter notebook
```
Open any notebook in the `analysis/` folder and run all cells.
