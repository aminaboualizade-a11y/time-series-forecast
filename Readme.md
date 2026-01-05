# Time-Series Forecasting & Risk Analysis (AAPL)

This project applies time-series modeling and risk analysis techniques to AAPL daily stock returns. The goal is to understand market behavior, forecast short-term returns, and convert those forecasts into forward-looking risk estimates such as Value-at-Risk (VaR).

This project is part of my Quant / Risk Analyst learning path and focuses on practical, industry-relevant methods.

---

## 🎯 Objectives

- Convert price data into daily returns and rolling volatility  
- Fit an ARIMA model to daily returns  
- Forecast short-term expected returns  
- Analyze residuals for randomness and volatility clustering  
- Compute **95% daily VaR** from the model forecast  
- Compare historical vs forecast risk

---

## 📊 Data

- **Ticker:** AAPL
- **Source:** Yahoo Finance
- **Frequency:** Daily (Business Days)

Data is saved locally in:



---

## 🧪 Methods

### 1️⃣ Data Preparation
- Download AAPL Adjusted Close prices
- Convert to daily percentage returns
- Compute 21-day rolling annualized volatility

### 2️⃣ ARIMA Forecasting
- Fit **ARIMA(1,0,1)** to daily returns
- Forecast 30-day returns
- Plot expected return + confidence intervals

### 3️⃣ Residual Diagnostics
- Check mean ≈ 0  
- Inspect distribution shape  
- Review autocorrelation  
- Identify volatility clustering  

### 4️⃣ Risk Estimation (VaR)
- Estimate residual volatility  
- Assume returns ≈ normal around forecast mean  
- Compute **95% Value-at-Risk (VaR)**  
- Compare with historical VaR  

---

## 📌 Key Results

| Metric | Value |
|-------|-------|
| Daily Volatility (std) | **~1.79%** |
| Historical 95% VaR | **~–2.89%** |
| Forecast 95% VaR | **~–3.06%** |

### Interpretation

- Expected daily returns are close to zero  
- But downside risk remains meaningful  
- Roughly **1 in 20 trading days** may see losses beyond ~3%  
- Forecast VaR is slightly more conservative than historical VaR  
- Suggesting **modestly elevated risk ahead**

This aligns with real-world financial behavior:
markets are hard to predict in direction,  
but **risk is measurable and time-varying**.




---

## 🛠 Tools & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- statsmodels (ARIMA)
- Jupyter Notebook

---

## 🧠 Key Learning Takeaways

- Stock returns are difficult to predict → **low predictive mean**
- Risk remains → **non-zero volatility**
- Residuals show:
  - heavy tails  
  - volatility clustering  
- VaR converts volatility into **downside risk estimates**
- Forward-looking risk ≠ historical risk

---

## 👤 Author

**Amin Abooaliadeh**  
Aspiring Quant & Risk Analyst — Toronto, Canada  

