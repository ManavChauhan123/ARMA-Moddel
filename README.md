# ARMA Model for Time Series Analysis

## Overview
This project implements **Autoregressive Moving Average (ARMA) models** for financial time series forecasting using Python. The ARMA model is an essential tool in statistical time series analysis, used to model and predict financial asset prices based on historical data.

## Table of Contents
1. **Time Series Basics**
   - Trend, Cycle, and Seasonality
   - Log Price Properties
   - Linear Regression for Trend Estimation
2. **Autoregressive (AR) and Moving Average (MA) Models**
   - AR Model
   - MA Model
3. **ARMA and ARIMA Models**
   - ARMA Model
   - ARIMA Model (for non-stationary data)

## Features
- **Trend and Seasonality Analysis**: Uses historical stock data to visualize price trends and seasonality.
- **Stationarity Testing**: Conducts the Augmented Dickey-Fuller (ADF) test to determine if a time series is stationary.
- **AR, MA, ARMA, and ARIMA Model Implementations**: Implements predictive models for financial time series forecasting.
- **Backtesting Strategy Performance**: Evaluates trading strategies based on predicted values.

## Dependencies
To run this project, install the following Python libraries:
```bash
pip install numpy pandas matplotlib yfinance statsmodels
```

## Implementation Details
### Data Import and Preprocessing
- Uses `yfinance` to fetch stock data (e.g., Google and EUR/USD exchange rate).
- Converts price data into returns for stationarity.
- Conducts logarithmic transformation for log-price analysis.

### AR, MA, ARMA, and ARIMA Models
- **Autoregressive Model (AR)**: Uses past values to predict future prices.
- **Moving Average Model (MA)**: Uses past forecast errors to improve predictions.
- **ARMA Model**: Combines AR and MA models for stationary data.
- **ARIMA Model**: Extends ARMA by adding differencing for non-stationary data.

### Backtesting
- Uses a simple trading strategy based on predicted price movements.
- Evaluates performance with key metrics:
  - **Sharpe Ratio**
  - **Sortino Ratio**
  - **Maximum Drawdown**
  - **Value at Risk (VaR) and Conditional VaR (cVaR)**

## Results
- **AR Model**: Weak predictive power for EUR/USD returns.
- **MA Model**: Moderate performance with better Sharpe ratio.
- **ARMA Model**: Outperforms AR and MA with a higher Sharpe ratio.
- **ARIMA Model**: Performs slightly worse due to overfitting.


