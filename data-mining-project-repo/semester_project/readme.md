# Stock Price Prediction Project

## 1. Overview

The project aims to predict future stock prices using machine learning models. We begin with traditional regression and will evolve towards deep learning architectures like LSTM for more robust time-series modeling.

## 2. Project Structure
````
1. data_cleaning.ipynb: Cleans and preprocesses raw historical stock data from yahoo finance
2. data_exploration_stock_price.ipynb: Performs exploratory data analysis (EDA), visualizations, and feature inspection
3. model_regression_ridge.ipynb: Implements Ridge Regression for baseline prediction for single ticker 
4. lstm_prediction.ipynb: Deep learning-based LSTM model for time-series forecasting 
````

## 3. Data Source
- Yahoo Finance API via yfinance Python library
- Tickers used include: AAPL, MSFT, with flexibility to scale to others

## 4. Data Cleaning
- a. Removal of missing values
- b. Target generation using next-day Open and Close prices
- c. Min-Max Scaling of all numeric features
- d. Multi-index to single-index conversion for ticker-aware modeling


## 5. Data Exploration
- a. Time-series line plots of Close prices per ticker
- b. Volume spikes and trend correlations
- c. Target distribution visualized across time and assets

## 6. Features Used
- a. Raw Market Features: Open, High, Low, Close, Volume
- b. Target Variables: target_next_close

## 7a. Models Used
- a. Ridge Regression (Baseline): Predicts target_next_close; Simple, interpretable, and performs reasonably well on structured data. 
- b. LSTM (Long Short-Term Memory): For sequential pattern learning across historical prices
   
## 7b. Forecasting
- Forecasted the close price for the next 5 days. 

## 8. Future Scope for self-learning
Try different architectural models, may include but not limited to: 
- Autoencoders: For feature compression or anomaly detection
- Transformer Networks: For attention-based time-series modeling across multiple assets
- Ticker Embedding: To incorporate ticker identity directly into the model
- Sentiment analysis to study the impact of news on the volatility of the share price. 

## 9. Goal
built the pipeline that ingested historical market data, learns general and ticker-specific behavior, and predictions/forecast next 5 day close price.