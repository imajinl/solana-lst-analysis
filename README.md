# LST Comparative Analysis: jitoSOL, mSOL, bSOL

This repository presents a structured analysis of leading Solana Liquid Staking Tokens (LSTs): **jitoSOL**, **mSOL**, and **bSOL**, focusing on performance, liquidity behavior, trading metrics, TVL, and APR. The research leverages clean, standardized data to provide a consistent and reliable comparison across assets.

---

## 📊 Methodology

The core analytical pillars include:

- **Consistent Liquidity Source**: All liquidity-related analysis is derived from **Kamino Finance**. Kamino deploys nearly all liquidity at the **market midpoint**, making it the most homogeneous and least noisy source of liquidity data across LSTs.
- **VWAP-Based Normalization**: Prices are normalized using **4-hour volume-weighted average prices (VWAP)** to mitigate the effects of low-liquidity outliers and better reflect actual execution-weighted prices over time.
- **Time-Bucketed Metrics**: Trading activity and performance data are aggregated in 4-hour intervals to strike a balance between granularity and readability.
- **Relative Performance Benchmarks**: All assets are rebased to a common starting point for return and volatility comparisons.

---

## 📁 Notebooks

### 1. `LST Metrics - jitoSOL, mSOL, bSOL - [2025-08-05].ipynb`

Focus:
- Computes advanced metrics such as volatility, max drawdown, and trading behavior metrics.
- Analyzes trading volumes, trade count, and average trade sizes.
- Uses 4-hour interval VWAP pricing from Kamino to ensure consistent comparisons.

### 2. `LST Performance - jitoSOL, mSOL, bSOL - [2025-08-05].ipynb`

Focus:
- Tracks cumulative and normalized returns over time vs. SOL.
- Highlights relative outperformance or underperformance periods vs. SOL.
- Applies VWAP-derived price normalization to isolate core performance trends.

### 3. `LST TVL, APR - jitoSOL, mSOL, bSOL - [2025-08-05].ipynb`

Focus:
- Plots the Total Value Locked (TVL) over time for each LST.
- Tracks historical Annual Percentage Rate (APR) data for yield comparison.
- Highlights yield divergence patterns and TVL trends across protocols.

---

## 📌 Data Sources

The datasets used in this analysis are aggregated from:

- **Dune Analytics**: For VWAP prices, trade volume, trade counts, and average trade sizes (based on structured time-series data from LST trading pools).
- **DeFiLlama**: For TVL and APR data on jitoSOL, mSOL, and bSOL.

All data is aggregated in **4-hour time buckets**, enabling more responsive and detailed tracking of market dynamics without excessive noise.

---

## 💡 Key Assumptions

- **Only Kamino liquidity** is considered for liquidity metrics to make liquidity 'fungible.'
- **VWAP normalization** is used to eliminate noise from outlier trades and better represent practical pricing.
- **Trading activity metrics** are based on actual executed volume and filled trade counts.

---

## 🔧 Dependencies

To run the notebooks, install the required Python packages:

```bash
pip install pandas numpy matplotlib seaborn
