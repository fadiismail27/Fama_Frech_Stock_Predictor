# Fama-French Stock Predictor 

A Python-based stock return prediction model I built to explore quantitative finance and learn how institutional investors think about risk. It uses the Fama-French three-factor framework to decompose and analyze historical equity returns for AAPL, MSFT, and GOOGL over 2010–2024.

---

## Why I Built This

I've always been curious about how hedge funds and quant firms actually model stock returns beyond just "the market went up." The Fama-French model was one of the first things I came across that felt like real finance, not just buy low sell high, but a rigorous statistical framework for understanding *why* a stock moves the way it does. I built this project to get hands-on with the math and see how the factors play out on real data.

---

## What It Does

Extends classic CAPM by regressing each stock's excess return on three systematic risk factors:
```
Rᵢ − Rf = αᵢ + β₁(Rm − Rf) + β₂·SMB + β₃·HML + εᵢ
```

- **Market beta** — how sensitive the stock is to broad market swings
- **SMB** (Small Minus Big) — size factor exposure
- **HML** (High Minus Low) — value vs. growth exposure
- **Alpha** — return unexplained by the three factors

The output tells you, for example, that GOOGL behaves like a growth stock (negative HML beta), which matches intuition and was cool to see fall out of the regression naturally.

---

## Tech Stack
`yfinance` · `pandas` · `numpy` · `statsmodels` · `matplotlib`

---

## What I Learned

- How to work with financial time series data and handle things like adjusted closes and missing trading days
- Running and interpreting OLS regression in a finance context
- That even a three-factor model leaves a lot of alpha unexplained, which makes me want to explore more factors (momentum, profitability) down the line
