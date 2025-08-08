# LST Comparative Analysis: jitoSOL, mSOL, bSOL

This repository presents a structured analysis of leading Solana Liquid Staking Tokens (LSTs): **jitoSOL**, **mSOL**, and **bSOL**, focusing on performance, liquidity behavior, trading metrics, TVL, and APR. The research leverages clean, standardized data to provide a consistent and reliable comparison across assets.

---

## 📊 Methodology

The core analytical pillars include:

- **Consistent Liquidity Source**: All price- and liquidity-related analysis is derived from **Kamino Finance**. Kamino deploys nearly all liquidity at the **market midpoint**, making it the most homogeneous and least noisy source of liquidity data across LSTs.
- **VWAP-Based Normalization**: Prices are normalized using **4-hour volume-weighted average prices (VWAP)** to mitigate the effects of low-liquidity outliers and better reflect actual execution-weighted prices over time.
- **Time-Bucketed Metrics**: Trading activity and performance data are aggregated in 4-hour intervals to strike a balance between granularity and readability.
- **Relative Performance Benchmarks**: All assets are rebased to a common starting point for return and volatility comparisons.

---

## 📁 Notebooks

### 1. `LST Metrics - jitoSOL, mSOL, bSOL - [2025-08-05].ipynb`

Focus:
- Computes advanced metrics such as volatility, Sharpe ratio, and max drawdown.
- Analyzes trading volumes, trade count, and average trade sizes.
- Uses 4-hour interval VWAP pricing from Kamino to ensure consistent comparisons.

### 2. `LST Performance - jitoSOL, mSOL, bSOL - [2025-08-05].ipynb`

Focus:
- Tracks cumulative and normalized returns over time.
- Highlights relative outperformance or underperformance periods.
- Applies VWAP-derived price normalization to isolate core performance trends.

### 3. `LST TVL, APR - jitoSOL, mSOL, bSOL - [2025-08-05].ipynb`

Focus:
- Time series of **Total Value Locked (TVL)** per LST.
- Tracks changes in **Annual Percentage Rate (APR)** to study yield trends.
- Investigates correlation between yield fluctuations and TVL migration.

---

## 📌 Data Sources

The datasets used in this analysis are aggregated from:

- **Dune Analytics**: For VWAP prices, trade volume, trade counts, and average trade sizes (based on structured time-series data from LST trading pools).
- **DeFiLlama**: For TVL and APR data on jitoSOL, mSOL, and bSOL.

All data is aggregated in **4-hour time buckets**, enabling more responsive and detailed tracking of market dynamics without excessive noise.

---

## 💡 Key Assumptions

- **Only Kamino liquidity** is considered for price-based metrics to ensure fair, midpoint-based price discovery across all tokens.
- **VWAP normalization** is used to eliminate noise from outlier trades and better represent practical pricing.
- **Trading activity metrics** are based on actual executed volume and trade counts, not order book snapshots.

---

## 📈 Use Cases

This repository may be useful for:

- Researchers and analysts comparing LST protocols on Solana.
- Portfolio managers benchmarking staking derivatives.
- Developers building dashboards or alert systems for LST performance and trading metrics.

---

## 🔧 Dependencies

To run the notebooks, install the required Python packages:

```bash
pip install pandas numpy matplotlib seaborn
