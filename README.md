# Algorithmic Trading System

## Overview
This project implements a machine learning based algorithmic trading pipeline that retrieves historical market data, generates predictive features, trains a model, and evaluates a trading strategy using Alpaca's paper trading environment.

The objective is to study whether short-term price movements can be predicted using momentum-based features and to simulate a systematic trading strategy.

---

## Features

- Historical market data retrieval using Alpaca API  
- Minute-level price data processing  
- Momentum-based feature engineering  
- Random Forest model for price movement prediction  
- Strategy backtesting and performance evaluation  
- Paper trading simulation

---

## Data Pipeline

Market data is retrieved using Alpaca's `StockHistoricalDataClient` and stored locally in **Parquet format** for efficient storage and retrieval.  
Data is organized per ticker and sorted by timestamp before feature generation.

---

## Model

The trading signal is generated using a **Random Forest classifier** trained on momentum-based features calculated across multiple time intervals.

The model predicts short-term forward returns and generates trading signals based on prediction confidence.

---

## Backtesting

Strategy performance is evaluated through historical simulations using metrics such as:

- Cumulative returns
- Daily returns
- Feature importance

---

## Tech Stack

- Python  
- pandas  
- NumPy  
- scikit-learn  
- Alpaca API  

---

## Future Improvements

- Add additional technical indicators (RSI, Bollinger Bands)
- Improve risk management and position sizing
- Experiment with advanced ML models
- Include transaction cost modeling

---

## Disclaimer

This project is for research and educational purposes only.  
All trades were executed in a paper trading environment.
