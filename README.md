# 🛡️ Portfolio Optimization and Simulation Under Geopolitical Risk

## 📌 Executive Summary

Using historical data from December 2018 to December 2021, I built a minimum-volatility portfolio from five ETFs tied to commodities, energy, gold, materials, and China technology; calibrated for a geopolitical risk scenario. The portfolio was then tested against real market data from January 2022 onward and stress-tested using 1,000 Monte Carlo simulation paths.

**Result:** The portfolio outperformed the S&P 500 by ~7 percentage points (29.4% vs 22.6%) during the out-of-sample period while maintaining virtually identical volatility. The actual 2023–2025 return placed in the **100th percentile** of simulated outcomes, validating the geopolitical hedge thesis.

---

## 📊 Data Information

| Parameter | Details |
|-----------|---------|
| **Source** | Yahoo Finance + FRED (Canadian 10Y bond rate) |
| **Estimation period** | Dec 2018 – Dec 2021 (weekly frequency) |
| **Out-of-sample period** | Jan 2022 – Jan 2025 |
| **Tickers** | IAU (Gold), VDE (Energy), XLB (Materials), DBC (Commodities), CQQQ (China Tech) |
| **Benchmark** | S&P 500 (`^GSPC`) |

---

## 📈 Key Results

**Out-of-Sample Performance (Jan 2022 – Jan 2025)**

| Metric | Portfolio | S&P 500 |
|--------|-----------|---------|
| Cumulative Return | **29.4%** | 22.6% |
| Annualized Volatility | 8.18% | 7.95% |

**Monte Carlo Simulation (2-Year Horizon, 1,000 Paths)**

| Metric | Value |
|--------|-------|
| Mean final value | $100.48 |
| 5% VaR | $95.73 |
| Actual outcome (2023–2025) | **$114.98 → 100th percentile** |

**What this means for business:**
The outperformance was concentrated, not broad-based. VDE (40% allocation) returned 68.5% as the Ukraine conflict triggered an energy price surge, that position carried the portfolio. XLB contributed almost nothing (0.08%) and CQQQ detracted (-35.9%). The portfolio worked because the position most tied to the geopolitical thesis delivered, and the weight structure limited damage from the ones that didn't.
The Monte Carlo result reinforces a key principle: the actual 2023–2025 return placed in the 100th percentile of simulated outcomes not because the model failed, but because the market entered a regime historical data couldn't anticipate. Knowing where a model's predictive power ends is as valuable as building the model itself.

---

## 🛠️ Technologies Used

`Python` · `pandas` · `numpy` · `matplotlib` · `yfinance` · `statsmodels` · `scipy.optimize`

**Methods:** Modern Portfolio Theory · CAPM (OLS) · Geometric Brownian Motion · Cholesky Decomposition · Value at Risk (VaR & CVaR)

---

## 🧭 Reflections and Learnings

- **Historical optimization doesn't guarantee future contribution.** XLB was selected for its low beta and low cross-asset correlations during the estimation window, both legitimate risk-reduction properties. Out-of-sample it returned virtually nothing (0.08%), a reminder that the optimizer minimizes past variance, not future underperformance.
- **Model error vs. regime shift.** The 100th percentile actual result is not a sign the model failed, it captured pre-crisis dynamics accurately. The market simply moved into territory that historical data couldn't anticipate. Learning to distinguish these two cases is one of the most practically valuable skills in applied data science.

This work was developed as part of my Management Analytics Master's program at Queen's University.

---

## 👩‍💻 About the Author

Hi! I'm Cynthia Gaspar, a business professional pursuing a Master's degree in Management Analytics at Queen's University. I am passionate about understanding real-world problems through data. Let's connect!

🔗 [LinkedIn](https://www.linkedin.com/in/cynthia-gaspar)
🔗 [Substack](https://substack.com/@cynthiagaspar)
