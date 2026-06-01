# Trader Performance vs Bitcoin Fear & Greed Index

## Overview

This project analyzes the relationship between **trader performance** (from Hyperliquid historical trade data) and **market sentiment** (Bitcoin Fear & Greed Index). The goal is to uncover patterns that can drive smarter, sentiment‑aware trading strategies.

The analysis includes:

- Cleaning and merging two datasets by date.
- Daily aggregation of trader PnL, win rate, volume, and trade count.
- Visual and statistical comparison of performance across Fear / Neutral / Greed days.
- Trader segmentation: identifying characteristics of profitable vs unprofitable traders.
- Time‑series analysis of cumulative PnL vs sentiment index.
- Actionable trading recommendations based on empirical findings.

---

## Datasets

1. **Hyperliquid Historical Trader Data** (`historical_data.csv`)  
   - Columns include: `Account`, `Coin`, `Execution Price`, `Size USD`, `Side`, `Timestamp IST`, `Closed PnL`, etc.  
   - Only rows with non‑zero `Closed PnL` (realized trades) are used.

2. **Bitcoin Fear & Greed Index** (`fear_greed_index.csv`)  
   - Columns: `timestamp`, `value` (0–100), `classification` (Fear / Greed / Neutral), `date`.  
   - Provided via Google Drive link.

---

## Requirements

- Python 3.8+
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `gdown`, `plotly` (optional)

Install all dependencies:

```bash
pip install pandas numpy matplotlib seaborn scipy gdown plotly
