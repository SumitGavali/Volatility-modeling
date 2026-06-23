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

### key note:- 
here forecasting window is of 50 and rolling mean is 20 at very first while building this the graphs of forecast overlaps so i am not abe to make distinction betwee them.
---

## Visual Results

### Real data

<img width="825" height="372" alt="image" src="https://github.com/user-attachments/assets/ee6a560c-5b77-479c-9809-21cda2678534" />

### Log return 
<img width="824" height="498" alt="image" src="https://github.com/user-attachments/assets/bc5479f5-5749-4f85-a5aa-4632e5a89256" />

### squared return
<img width="825" height="371" alt="image" src="https://github.com/user-attachments/assets/38d46cc7-67f2-47db-be19-2f8442e2ec2a" />

### adf test
<img width="344" height="356" alt="image" src="https://github.com/user-attachments/assets/0511d828-b81d-4c75-8578-346e0247cfee" />

<img width="574" height="651" alt="image" src="https://github.com/user-attachments/assets/086b7e57-a083-4492-9a07-89406d2c93ad" />

here is the right choice of direction

<img width="762" height="695" alt="image" src="https://github.com/user-attachments/assets/db589db5-207a-44cc-b758-ebc061b26893" />

### GARCH result
<img width="578" height="394" alt="image" src="https://github.com/user-attachments/assets/e0b3aacf-e7b9-4757-b38d-af21ed40bae3" />

### GARCH Conditional Volatility
<img width="826" height="383" alt="image" src="https://github.com/user-attachments/assets/04fca76c-5bc9-4dc5-a0a9-762b60040566" />


### Model Comparison

<img width="826" height="385" alt="image" src="https://github.com/user-attachments/assets/ec1cfa88-afd3-4ea7-86df-d27652d644db" />

### forecasting on test data 2025-2026(mid june)
<img width="826" height="362" alt="image" src="https://github.com/user-attachments/assets/ee48a0b5-bb0a-4771-9c9a-72cc21a01d91" />

### Forecast errors
<img width="823" height="355" alt="image" src="https://github.com/user-attachments/assets/ac1eceb9-89a6-4ba6-a1f0-f1123dab3bdd" />


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
