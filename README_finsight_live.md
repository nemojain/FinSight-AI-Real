# 📡 FinSight AI v2 - Live Market Data Analytics

> **Real-time quantitative analytics pipeline** pulling live OHLCV market data from Yahoo Finance via `yfinance`, computing institutional-grade risk metrics, and generating AI-powered insights using the Anthropic Claude API; across 3 years of actual market history (2022–2024).

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![yfinance](https://img.shields.io/badge/yfinance-Live%20Data-00843D?style=flat&logo=yahoo&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-150458?style=flat&logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-5.18+-3F4F75?style=flat&logo=plotly&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-1.24+-013243?style=flat&logo=numpy&logoColor=white)
![Claude API](https://img.shields.io/badge/Claude-Sonnet_4-D97706?style=flat&logo=anthropic&logoColor=white)
![Data](https://img.shields.io/badge/Data-Yahoo%20Finance%20(Real)-brightgreen?style=flat)

> 🔗 **Looking for the simulation-based version?** → [FinSight AI v1 - GBM Simulation Engine](https://github.com/nemojain/FinSight-Ai)

---

## 📌 v1 vs v2 - What Changed

| | FinSight AI v1 (GBM) | FinSight AI v2 (Live) |
|---|---|---|
| Data source | Synthetic -> Geometric Brownian Motion | Real -> Yahoo Finance via yfinance |
| Data granularity | Minute-level ticks | Daily OHLCV |
| Records | 491,400+ simulated | ~750 real trading days × 5 tickers |
| Market events | Simulated drift & volatility | Real - 2022 selloff, 2023 AI rally, NVDA surge |
| Reproducibility | Identical every run (seeded) | Updates daily as new data arrives |
| Skewness & kurtosis | Symmetric (GBM assumption) | Real fat tails and negative skew |

---

## 🧠 What This Project Does

- 📡 **Pulls 3 years of real OHLCV data** from Yahoo Finance using `yfinance` — no manual downloads
- 📊 **Computes institutional risk metrics** from real returns: Sharpe ratio, VaR 95%/99%, Max Drawdown, Rolling Volatility
- 🕯️ **Interactive candlestick charts** with MA20/MA50 overlays and real volume bars
- 📉 **Return distribution analysis** - shows real negative skew and fat tails that GBM cannot replicate
- 🔗 **Correlation matrix** computed from actual daily returns
- 📅 **Real market event annotations** - Fed rate hikes, 2022 bottom, NVDA AI earnings, 2023 rally
- 💹 **VWAP approximation** computed from real high/low/close/volume
- 💼 **Equal-weight portfolio** with real cumulative returns and drawdown attribution
- 🤖 **Anthropic Claude API** for natural-language analysis grounded in real market data

---

## 📅 Key Market Events Captured in the Data

| Date | Event | Impact |
|------|-------|--------|
| Jun 2022 | Fed hikes rates 75bps | Broad selloff across all 5 tickers |
| Oct 2022 | Market bottom | AAPL, MSFT hit cycle lows |
| Jan 2023 | Recovery rally begins | Tech leads rebound |
| May 2023 | NVDA AI earnings beat | NVDA surges 25%+ in a single session |
| 2024 | AI boom continues | NVDA, META outperform significantly |

---

## 🗂️ Project Structure

```
finsight-ai-live/
├── 📓 finsight_ai_real.ipynb    # Main analytics notebook
├── 📄 README.md
└── 📦 requirements.txt
```

---

## 📊 Sample Output Metrics (2022–2024, Equal Weight Portfolio)

> Note: Exact values update each run as Yahoo Finance data refreshes.

| Metric | Approximate Value |
|--------|------------------|
| 🏷️ Tickers | AAPL · MSFT · GOOGL · NVDA · META |
| 📅 Period | Jan 2022 – Dec 2024 (daily OHLCV) |
| 🗃️ Real data points | ~3,750 (750 days × 5 tickers) |
| 📉 2022 Max Drawdown | ~-35% (rate hike selloff) |
| 📈 Best performer | NVDA (AI earnings driven) |
| 🔗 Highest correlation | MSFT ↔ GOOGL |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| 🐍 Python 3.10+ | Core language |
| 📡 yfinance | Live OHLCV data from Yahoo Finance |
| 🔢 NumPy | Statistical computation |
| 🐼 Pandas | Time-series resampling & aggregation |
| 📈 Plotly | Interactive candlestick, histogram, heatmap charts |
| 🤖 Anthropic Claude API | AI-generated insights grounded in real market data |
| 📓 Jupyter Notebook | Interactive analysis environment |

---

## 🚀 How to Run Locally

**1️⃣ Clone the repo**
```bash
git clone https://github.com/nemojain/finsight-ai-live.git
cd finsight-ai-live
```

**2️⃣ Install dependencies**
```bash
pip install -r requirements.txt
```

**3️⃣ Launch Jupyter**
```bash
jupyter notebook
```

**4️⃣ Open `finsight_ai_real.ipynb` → Kernel → Restart & Run All**

> Data pulls automatically from Yahoo Finance - requires internet connection.  
> 💡 To enable AI insights, paste your Anthropic API key in the last cell.  
> Get a free key at: [console.anthropic.com](https://console.anthropic.com)

---

## 🎯 Skills Demonstrated

- ✅ Live data pipeline engineering with `yfinance` API
- ✅ Real market time-series analysis with Pandas
- ✅ Institutional risk metrics from real returns (Sharpe, VaR, Drawdown)
- ✅ Market event identification and annotation
- ✅ Fat tail and skewness analysis on real return distributions
- ✅ VWAP computation from real OHLCV data
- ✅ Interactive financial visualization with Plotly
- ✅ AI integration via Anthropic Claude API with real data context

---

## 🔗 Related Projects

| Project | Description | Link |
|---------|-------------|------|
| 📈 FinSight AI v1 | Same analytics stack - GBM simulation engine | [FinSight-Ai](https://github.com/nemojain/FinSight-Ai) |
| 📊 PerfIQ FP&A | Enterprise financial planning — 504k+ GL transactions | [fpa-command-center](https://github.com/nemojain/fpa-command-center) |

---

⭐ *If you found this useful, consider giving it a star!*
