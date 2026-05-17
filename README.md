# FOMO Behavior Analysis in Cryptocurrency Investors

## Overview

This project focuses on analyzing and quantifying FOMO (Fear of Missing Out) behavior among cryptocurrency investors using data analysis and machine learning techniques.

The study combines blockchain transaction data, market indicators, and community interest signals to identify different levels of FOMO behavior in Bitcoin investors.

## Objectives

* Analyze investor trading behaviors in the cryptocurrency market.
* Extract behavioral features related to FOMO.
* Cluster investors into different FOMO levels.
* Build machine learning models to classify investor behavior.

## Dataset

The project integrates multiple datasets:

* **BABD-13 dataset**: Bitcoin wallet transaction information.
* **On-chain transaction data** collected via Blockchain API.
* **Market data** from CoinMarketCap:

  * OHLCV
  * Market Capitalization
  * Circulating Supply
* **Google Trends** data using `pytrends`.
* **Realized Cap** data from bitview.space.

## Data Processing

The preprocessing pipeline includes:

* Handling missing values
* Removing non-numeric features
* Feature scaling using **StandardScaler**
* Correlation analysis and feature selection

## Feature Engineering

Behavioral features were designed to quantify FOMO-related actions, including:

* `chasing_ratio`
* `chasing_intensity`
* `trade_accel_7d`
* `trade_accel_30d`
* `trade_accel_ratio`
* `reaction_speed`
* `reaction_rate`
* `inconsistency_by_volume`
* `inconsistency_by_event`
* `drawdown_sensitivity`

## Methodology

### 1. Clustering

Unsupervised learning methods were used to identify investor behavior groups:

* K-Means
* DBSCAN
* HDBSCAN
* Gaussian Mixture Model (GMM)

Evaluation metrics:

* Silhouette Score
* Davies-Bouldin Index
* Calinski-Harabasz Score

### 2. Classification

After clustering, investors were categorized into:

* Low FOMO
* Medium FOMO
* High FOMO

Classification models:

* XGBoost
* Decision Tree
* Random Forest

Evaluation metrics:

* Accuracy
* Precision
* Recall
* F1-score

## Results

* XGBoost achieved the best performance with approximately:

  * Accuracy: 96.7%
  * F1-score: 0.97

Key findings:

* High-FOMO investors account for approximately 27% of wallets.
* High-FOMO behavior is associated with:

  * Very fast reaction times
  * High chasing ratios
  * Strong responses to market fluctuations


## Future Work

* Improve behavioral feature engineering.
* Apply the framework to real-time transaction streams.
* Extend the model to other cryptocurrencies and financial markets.

