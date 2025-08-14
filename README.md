# 18.642
Mathematics with Applications in Finance
# Project Title
**Dynamic Portfolio Optimization Trading Strategy**

## Course
Mathematics with Applications in Finance (MIT 18.642)

## Date
Fall 2023

---

## Summary
- Built a dynamic portfolio optimization model for 31 S&P 500 stocks using **Julia** and **Gurobi**, maximizing Sharpe ratio with constraints on volatility (<5% monthly) and position size (<10%).
- Implemented rolling 5-year estimation windows for expected returns, betas, and covariance matrices; backtested from 2007–2022 against S&P 500 and equal-weight benchmarks.
- Achieved **7.90% annualized return**, slightly outperforming the S&P 500 (7.67%) over 15 years; factor regression identified **AAPL, NVDA, BLK, AMZN, and BAC** as key return drivers.
- Demonstrated skills in **financial modeling, time series analysis, quantitative backtesting**, and **risk management integration**.

---

## Goal / Problem Statement
Construct an optimal portfolio of 31 S&P 500 companies using optimization methods (Gurobi in Julia) to maximize the Sharpe ratio under specific constraints, and dynamically adjust the portfolio annually based on rolling market data from 2002–2022.

---

## Methods / Tools
**Languages/Software**: Julia, Excel  
**Libraries**: Gurobi Optimizer  

**Data**:
- Monthly returns from CRSP via WRDS for 31 selected S&P 500 stocks, S&P 500 index, 10-year Treasury yield as risk-free rate
- Calculated additional factors from raw returns data, including:
  - Beta for each stock
  - Expected future return (using CAPM)
  - Correlation between stocks
  - Industry classification

**Steps**:
1. Modern Portfolio Theory
2. Sharpe ratio maximization
3. Portfolio weight tables and return attribution
4. Constraints: max 10% per stock, target portfolio volatility < 5% monthly, weights sum to 1
5. Rolling 5-year estimation windows for beta, covariance, and expected return
6. Backtesting from 2007–2022 against S&P 500 and equal-weight benchmark
7. Factor regression for alpha testing

---

## Results
- Optimized portfolio Sharpe ratio slightly outperformed S&P 500 (**7.90% vs 7.67% annualized return**) over 15 years
- Equal-weight portfolio surprisingly outperformed both, suggesting strong stock selection effect
- Rolling rebalancing produced performance close to benchmark in most years; higher returns in some recovery years (e.g., 2009)
- Key contributors: **AAPL, NVDA, BLK, AMZN, BAC**

---

## Key Skills Demonstrated
- Financial modeling & optimization  
- Time series data analysis  
- Backtesting  
- Risk constraint integration  
- Statistical analysis of returns  

---

## Potential Extensions
- Fama-French 3-factor regression on monthly returns  
- Weighted time series (linear/exponential decay)  
- Industry allocation limits & transaction costs  
- Varying rolling window and holding periods  
- Expanded stock universes & historical periods  
