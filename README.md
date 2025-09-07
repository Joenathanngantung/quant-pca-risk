# Quant Project – PCA for Portfolio Risk

**Goal:** Apply Principal Component Analysis (PCA) to daily returns of 20 large-cap US equities to uncover hidden risk drivers, reduce dimensionality, and evaluate interpretability with Varimax rotation.

## Data
- **Assets (20 US large-caps):**
  - *Technology/Communication*: AAPL, MSFT, AMZN, GOOGL, META, NVDA, NFLX
  - *Financials/Payments*: JPM, GS, V, MA
  - *Industrials/Energy*: BA, GE, CAT, XOM, CVX
  - *Consumer/Other*: DIS, IBM, WMT, TSLA
- **Frequency:** Daily adjusted closing prices
- **Period:** January 2015 – January 2025 (\~2,500 observations)
- **Transformations:**
  - Returns computed as daily percentage changes
  - Returns standardized (z-scored) for PCA comparability

## Methods

- Correlation matrix (heatmap of return co-movements)
- PCA extraction (eigenvalues, variance explained)
- Scree plot + Kaiser criterion for component selection
- Factor loadings:
  - Heatmap (PC1–PC5)
  - Scatterplot (PC1 vs PC2)
- Factor returns (time series of PC scores)
- Covariance reconstruction (Frobenius norm error vs k)
- Varimax rotation (interpretability of first 3 PCs)

## Key Results

- **PC1 (market factor):** \~43% of variance → broad co-movement
- **PC2 (sector tilt):** \~13% of variance → Tech vs. Industrials/Energy split
- **PC3 (idiosyncratic):** \~9% of variance → Tesla & Nvidia dominance
- **Top 3 PCs explain \~65%**, top 5 \~75–80%
- **Covariance reconstruction:** 3–5 PCs approximate full risk matrix with minimal error
- **Varimax rotation:** clarified sector-based groupings without reducing variance explained

## Deliverables

* 📑 [Research Paper PDF](docs/pca_portfolio_risk.pdf)
* 📸 Figures in `docs/charts/`
* 📂 [Notebook](notebooks/pca_portfolio_risk.ipynb)
* 🖼️ [Summary Slide](docs/pca_portfolio_risk.png)
