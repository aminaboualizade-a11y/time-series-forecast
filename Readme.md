# Time-Series Forecasting & Risk Analysis (AAPL)

This project analyzes AAPL daily prices using time-series methods to:

- Compute returns and rolling volatility
- Fit an ARIMA model to daily returns
- Generate short-term forecasts
- Convert model output into forward-looking Value-at-Risk (VaR)

---

## 🎯 Objectives

- Understand how to transform price series into returns and volatility
- Apply ARIMA to model and forecast return dynamics
- Use model residuals to estimate volatility and compute 95% daily VaR
- Compare historical and forecast VaR in a risk-management context

---

## 📂 Project Structure

```text
time-series-forecast/
│
├── data/
│   ├── aapl_prices.csv
│   ├── aapl_returns.csv
│   └── arima_var_forecast.csv
│
├── notebooks/
│   └── 01_time_series_forecast.ipynb
│
├── outputs/
│   └── (optional charts / exports)
│
├── venv/
└── README.md



## 🧪 Methods

Data Preparation

Download AAPL Adjusted Close prices from Yahoo Finance (2015–2025)

Compute daily returns and 21-day rolling annualized volatility

## ARIMA Modeling

Fit an ARIMA(1,0,1) model to daily returns

Analyze residuals for autocorrelation and distribution shape

Risk Estimation (VaR)

Use residual volatility (std ≈ 1.79% daily) as input

Compute 95% daily VaR from the ARIMA forecast distribution

Compare historical VaR (~–2.89%) to forecast VaR (~–3.06%)

📊 Key Results

Daily volatility (residual std): ~1.79%

Historical 95% VaR: ~–2.89%

Average forecast 95% VaR: ~–3.06%

Interpretation:

Expected daily return is close to zero, but downside risk remains material.

VaR suggests that on ~1 out of 20 days, losses greater than ~3% can occur.

Forecast VaR is slightly more conservative than historical VaR, indicating modestly elevated expected risk.

🛠 Tech Stack

Python

Pandas, NumPy

Matplotlib

statsmodels (ARIMA)

Jupyter Notebook