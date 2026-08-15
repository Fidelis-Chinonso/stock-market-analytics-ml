# Stock Market Analytics and Machine Learning

This repository contains the computational work supporting a study of historical stock-market behaviour using financial data analytics and machine learning. The study examines historical price movements, volatility, trading activity, market direction, and selected temporal patterns across U.S. constituent stocks and NIFTY 50 securities.

The analysis combines exploratory financial analysis, financial feature engineering, and machine-learning techniques to examine both historical market characteristics and future market behaviour.

## Research Scope

The study uses two main datasets with different structures and historical coverage. The first is a U.S. constituent-stock dataset containing more than 3.5 million daily observations. The second is a NIFTY 50 dataset combining historical OHLCV observations with additional NSE trading-activity information.

The datasets are analysed separately because they provide different variables and market coverage.

## Analytical Components

The exploratory analysis examines differences in stock-level volatility, trading activity, market direction, price movement, and trading behaviour. Historical patterns are also examined across years and months to identify changes in market characteristics over time.

Financial feature engineering is used to derive variables from the original market data, including:

* Daily Return
* Price Range
* MA5
* MA20
* MA50
* Rolling Volatility
* Candlestick classifications
* Moving-average trading signals

These features provide additional measures of price behaviour, trend, and market activity for subsequent analysis and predictive modelling.

## Machine Learning

Two predictive tasks are developed in the study.

### 1. Constituent Stock Volatility Classification

The U.S. constituent-stock dataset is used to classify the volatility of the following trading day into three categories:

* Low
* Medium
* High

Logistic Regression and Decision Tree Classification are evaluated using accuracy, precision, recall, and F1-score.

The Decision Tree achieved the stronger overall classification performance, with an accuracy of **82.91%** and an F1-score of **0.8308**. Feature analysis identified **Price Range** and **MA50** as the most influential predictors.

### 2. NIFTY 50 Trading Volume Prediction

The Yahoo Finance component of the NIFTY 50 dataset is used to predict the trading volume of the following trading day.

Linear Regression and Decision Tree Regression are evaluated using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and the coefficient of determination (R²).

Linear Regression produced the stronger overall result, achieving an **R² of 0.728**, with an MAE of approximately **4.15 million** and an RMSE of approximately **14.94 million**. Current trading volume was the dominant predictor of subsequent trading volume in the Decision Tree analysis.


## Notebooks

| Notebook                                         | Description                                                                                                                                                          |
| ------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `01_constituent_data_analysis.ipynb`             | Exploratory analysis of the U.S. constituent-stock dataset, including volatility, trading activity, market direction, moving-average signals, and temporal patterns. |
| `02_nifty50_analysis.ipynb`                      | Analysis of NIFTY 50 OHLCV data and additional NSE trading-activity information.                                                                                     |
| `03_constituent_volatility_classification.ipynb` | Feature engineering, volatility-level classification, model development, evaluation, and feature-importance analysis using the constituent-stock dataset.            |
| `04_nifty50_volume_prediction.ipynb`             | Feature engineering, regression modelling, evaluation, and feature-importance analysis for next-day NIFTY 50 trading-volume prediction.                              |

## Data

The raw financial datasets are not included in this repository because of their size.

The constituent-stock dataset contains historical daily market observations for U.S. stocks. The NIFTY 50 data consists of historical OHLCV observations together with additional NSE market-activity variables, including turnover, traded quantity, number of trades, and deliverable quantity.

Users attempting to reproduce the analysis should obtain the corresponding datasets from their original sources and update the data paths in the notebooks where necessary.

## Technologies

The analysis was conducted using Python and commonly used data-science libraries, including:

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Reproducibility

The notebooks contain the data preparation, exploratory analysis, feature engineering, machine-learning development, and model evaluation procedures used in the study.

The notebooks were developed as part of an academic research project. Because the original datasets are not included in the repository, complete reproduction requires access to the corresponding source datasets.

## Purpose

This repository serves as the computational companion to the associated dissertation and provides the analytical and machine-learning procedures used to generate the reported findings.

## Author

**Fidelis Chinonso Okonkwo**

2026
