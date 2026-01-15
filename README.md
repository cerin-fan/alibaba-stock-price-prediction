# Alibaba Stock Price Prediction  
*Time Series Forecasting & Model Comparison*

## Project Overview

This project focuses on time series forecasting and model comparison using real-world financial data.  
Using Alibaba Group (BABA) stock prices as a case study, multiple machine learning and deep learning models were implemented and evaluated to assess their predictive performance and robustness in a practical forecasting setting.

## Analytical Problem

Financial time series are characterised by volatility and strong temporal dependencies, making accurate forecasting challenging.  
The objective of this project is to examine whether historical price information and engineered technical indicators can be used to predict future closing prices, and to compare how different modelling approaches perform under the same time-aware experimental setup.

## Data & Features

- **Data source**: Alibaba Group (NYSE: BABA) historical stock data retrieved via Yahoo Finance  
- **Time period**: 2014 – 2025  
- **Target variable**: Daily closing price  

To enrich the raw price data, several technical indicators were engineered, including:
- Relative Strength Index (RSI)
- Moving Average Convergence-Divergence (MACD)
- Bollinger Bands
- Stochastic Oscillator  

Time-related features were also encoded to capture cyclical patterns in the data.

## Methodology

All models were trained and evaluated using a consistent data processing pipeline and time-aware validation strategy to avoid data leakage.

The following modelling approaches were implemented and compared:
- XGBoost  
- Recurrent Neural Network (RNN)  
- Long Short-Term Memory (LSTM)  
- Gated Recurrent Unit (GRU)  
- 1D Convolutional Neural Network (1D-CNN)  

A sliding window approach was applied to construct time series inputs, and hyperparameters were tuned using grid search combined with time series cross-validation.

## Key Results & Insights

Model performance was evaluated using Mean Squared Error (MSE) and R-squared (R²).

- XGBoost demonstrated the strongest overall performance, showing higher accuracy and stability on this dataset.
- Deep learning models such as LSTM and GRU achieved reasonable predictive performance but were more sensitive to window size and hyperparameter choices.
- The results suggest that for medium-sized financial time series data, simpler tree-based models can outperform more complex deep learning architectures when robustness and interpretability are prioritised.

These findings highlight the importance of selecting models based on data characteristics rather than model complexity alone.

## Notes & Next Steps

This project focuses on historical price-based features and does not incorporate external factors such as macroeconomic indicators or financial news.  
Potential future improvements include integrating additional data sources, experimenting with ensemble methods, or exploring more advanced sequence models.

