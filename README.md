# 6BUIS017W CWK1: S&P 500 Stock Segmentation (RFM and Risk/Return)

Student ID: w2149468 | University of Westminster | CRM & CM with Business Intelligence

## Contents
- `6BUIS017W__w2149468.ipynb`: full analysis notebook (run top to bottom in Google Colab)
- `sp500_constituents_snapshot.csv`: S&P 500 constituent list as retrieved
- `exclusion_log.csv`: 12 excluded tickers with reasons
- `mean_weekly_return.csv`, `weekly_beta.csv`, `rfm_features.csv`: feature tables
- `risk_return_clusters.csv`, `rfm_clusters.csv`: cluster assignments (Ward and K-means, k = 4)
- `rfm_correlation_matrix.csv`: correlations among R, F and log1p(M)
- `sector_composition_*.csv`: sector crosstabs by cluster
- `*.png`: dendrograms, PCA cluster plots, sector composition chart

## Provenance
- Constituent list: Wikipedia, retrieved 23 November 2026 (503 tickers)
- Prices: Yahoo Finance via yfinance, 1 Jan 2021 to 1 Jan 2025 (end exclusive), benchmark ^GSPC
- Sample: 498 downloaded, 491 retained after validation, 481 in the clustering
- Weekly resampling: Friday-ending weeks (W-FRI), 207 observations
- RFM observation date: 31 December 2024; 60-session window; 20-session volume baseline
- Random seed: `random_state=42`, `n_init=10` for K-means

## Reproducing
Open the notebook in Colab and choose Runtime > Run all. The raw price cache
(`price_data_cache.pkl`, over 25 MB) is not included. Running the notebook regenerates it.

## Note
Clusters describe historical 2021 to 2025 behaviour. They are not predictive.

