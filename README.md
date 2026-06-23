# S&P 500 Volatility Forecasting using GARCH, EWMA and Rolling Volatility

## Overview

This project develops a quantitative volatility forecasting framework using 10 years of S&P 500 market data (2016–2026).

Unlike traditional stock prediction projects that attempt to forecast prices, this project focuses on forecasting market risk through conditional volatility modeling.

The study evaluates whether volatility clustering exists in equity markets and compares the forecasting performance of:

* GARCH(1,1)
* EWMA (RiskMetrics)
* 20-Day Rolling Volatility

---

## Business Objective

Financial institutions care less about predicting exact market direction and more about estimating future risk.

Volatility forecasts are used for:

* Value-at-Risk (VaR)
* Portfolio Risk Management
* Capital Allocation
* Derivatives Pricing
* Stress Testing

This project builds a complete volatility forecasting pipeline similar to workflows used by quantitative risk teams.

---

## Dataset

Source: Yahoo Finance

Instrument: S&P 500 Index (^GSPC)

Period: 2016 – 2026

Frequency: Daily

Observations: ~2,500 trading days

---

## Methodology

### Data Preparation

* Download S&P 500 data
* Compute logarithmic returns
* Perform exploratory analysis

### Statistical Validation

* Augmented Dickey-Fuller Test
* Autocorrelation Analysis
* ARCH-LM Test

### Volatility Modeling

* GARCH(1,1)
* EWMA (RiskMetrics)
* Rolling Volatility

### Model Validation

* Standardized Residual Analysis
* Ljung-Box Tests
* Out-of-Sample Backtesting

---

## Key Results

### Stationarity

ADF Statistic = -15.92

p-value < 0.001

Result:

Returns are stationary and suitable for volatility modeling.

---

### ARCH Effects

LM Statistic = 810.52

p-value < 0.001

Result:

Strong conditional heteroskedasticity detected.

---

### GARCH Parameters

ω = 0.0371

α = 0.1647

β = 0.8052

α + β = 0.9699

Result:

Market volatility exhibits strong persistence.

---

### Residual Diagnostics

Residual Ljung-Box p-value = 0.67

Squared Residual Ljung-Box p-value = 0.37

Result:

No significant autocorrelation remained after model fitting.

---

### Forecast Accuracy (RMSE)

| Model              | RMSE   |
| ------------------ | ------ |
| EWMA               | 0.2347 |
| GARCH              | 0.3125 |
| Rolling Volatility | 0.4201 |

Result:

EWMA achieved the strongest out-of-sample forecasting performance during the test period.

---

## Visual Results

### Volatility Clustering

[Insert squared returns chart]

### GARCH Conditional Volatility

[Insert conditional volatility chart]

### Model Comparison

[Insert Rolling vs EWMA vs GARCH chart]

---

## Technologies

Python

Libraries:

* Pandas
* NumPy
* Matplotlib
* Statsmodels
* Arch
* Scikit-Learn
* yfinance

---

## Repository Structure

```text
data/
notebooks/
images/
report/
README.md
```

---

## Future Work

* Value-at-Risk (VaR)
* Expected Shortfall (CVaR)
* Portfolio Risk Analytics
* Stress Testing Framework
* Multivariate GARCH Models

---

## Author

Sumit

Aspiring Quantitative Researcher | Data Science | Financial Analytics
