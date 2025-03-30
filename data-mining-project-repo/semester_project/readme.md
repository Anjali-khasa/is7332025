# Stock Price Prediction Project

## 1. Overview

The project aims to predict future stock prices using machine learning models. We begin with traditional regression and will evolve towards deep learning architectures like LSTM for more robust time-series modeling.

## 2. Project Structure
````
1. data_cleaning.ipynb: Cleans and preprocesses raw historical stock data from yahoo finance
2. data_exploration_stock_price.ipynb: Performs exploratory data analysis (EDA), visualizations, and feature inspection
3. model_regression_ridge.ipynb: Implements Ridge Regression for baseline prediction for single ticker 
4. lstm_prediction.ipynb: Deep learning-based LSTM model for time-series forecasting (in progress)
````

## 3. Data Source
Yahoo Finance API via yfinance Python library
Tickers used include: AAPL, MSFT, with flexibility to scale to others

## 4. Data Cleaning
a. Removal of missing values
b. Target generation using next-day Open and Close prices
c. Min-Max Scaling of all numeric features
d. Multi-index to single-index conversion for ticker-aware modeling


## 5. Data Exploration
a. Time-series line plots of Close prices per ticker
b. Volume spikes and trend correlations
c. Target distribution visualized across time and assets

## 6. Features Used
a. Raw Market Features: Open, High, Low, Close, Volume
b. Target Variables: target_next_close
c. Engineered (planned for LSTM): moving averages, RSI, volatility indicators, lagged features

## 7. Models Used
a. Ridge Regression (Baseline): Predicts target_next_close; Simple, interpretable, and performs reasonably well on structured data. 
b. Models in progress:
   LSTM (Long Short-Term Memory): For sequential pattern learning across historical prices
   XGBoost (Xtreme Gradient Boosting)
   
## 8. Future Scope
Try different architectural models, may include but not limited to: 
- Autoencoders: For feature compression or anomaly detection
- Transformer Networks: For attention-based time-series modeling across multiple assets
- Ticker Embedding: To incorporate ticker identity directly into the model

## 9. Goal
To build an pipeline that ingests historical market data, learns both general and ticker-specific behavior, and outputs next-day price predictions with explainability and scalability.