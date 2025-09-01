# Exchange Rate Forecasting & Purchasing Power Parity (PPP)

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 📌 Overview
This project analyzes the US–Japan exchange rate and tests the **Purchasing Power Parity (PPP)** hypothesis using time-series econometrics. It combines **absolute and relative PPP tests** with **Box–Jenkins ARIMA modelling** to study long-run parity, short-run dynamics, and to **forecast the real exchange rate**.  
Developed as part of the **MSc Business Analytics – Business Forecasting (EC6011)** coursework at **University College Cork**.

---

## 🔑 Key Features
- 10+ years of macro time series (USD/JPY, CPI-US, CPI-JP)
- **Data prep**: log transforms, differencing, stationarity testing (ADF)
- **PPP tests**:  
  - *Absolute PPP*: price level parity via OLS on CPI ratio  
  - *Relative PPP*: inflation differentials vs exchange rate changes
- **Forecasting**: ARIMA / SARIMAX (Box–Jenkins), VAR benchmark
- **Model selection**: AIC/BIC, residual diagnostics (Ljung–Box), stability checks
- **Interpretation**: parity evidence, shocks/structural breaks, forecast implications

---

## 🧰 Tech Stack
- **Python**
- **Libraries**: `pandas`, `numpy`, `matplotlib`, `statsmodels`
- **Environment**: Jupyter Notebook

---

## 🗂 Data
- **Exchange rate**: USD/JPY (monthly)
- **Inflation**: CPI (US, Japan)
- Source references: IMF/World Bank/FRED (documented in the report)

---

## 📊 Results (Snapshot)
- **Absolute PPP**: little to no support in levels (price ratio not a strong explainer).
- **Relative PPP**: weak/limited short-run parity; inflation differentials explain only a small share of variation.
- **Forecasting**: ARIMA(1,1,1) (or similar low-order ARIMA) selected by AIC/BIC; diagnostics indicate residual shocks/possible structural breaks → multivariate or regime models may further improve accuracy.
- **Takeaway**: PPP holds poorly in the short run; forecasting benefits from differencing and parsimonious ARIMA, while structural features merit richer models.

> For exact tables/figures and diagnostics, see the report.

---

## 🚀 How to Run

1. Clone the repository  
   ```bash
   git clone https://github.com/nikhil26vaddadi/exchange-rate-forecasting-ppp.git
   cd exchange-rate-forecasting-ppp
2. Install dependencies
   ```bash
   pip install -r requirements.txt
3. Run the notebook in Jupyter/Colab
   ```bash
   jupyter notebook EC6011-G3.ipynb
