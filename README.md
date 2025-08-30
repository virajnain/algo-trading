# Algo-Trading Strategies

This repository contains algorithmic trading strategies implemented in Python, along with backtesting and visualization tools. The project focuses on building, testing, and analyzing systematic trading strategies using historical stock data.

## Table of Contents

- [Introduction](#introduction)
- [Goals](#goals)
- [Strategy Architecture](#strategy-architecture)
- [Data Preprocessing](#data-preprocessing)
- [Backtesting](#backtesting)
- [Visualization](#visualization)
- [Future Work](#future-work)
- [Tools and Libraries](#tools-and-libraries)
- [License](#license)

## Introduction

Algorithmic trading relies on systematic strategies to make trading decisions. This project explores strategies such as Long/Short, momentum-based trading, and a Markov-chain-based candle streak strategy. The goal is to test these strategies using historical data and evaluate their performance before applying them to live markets.

## Goals

- Develop a modular framework for testing and deploying trading strategies
- Analyze strategy performance using standard metrics like return, volatility, Sharpe ratio, and drawdown
- Explore sequential and probabilistic approaches, including Markov chains for pattern recognition
- Visualize trades and equity curves to better understand strategy behavior
- Optimize strategies through parameter tuning and backtesting

## Strategy Architecture

- Strategies are implemented as classes, following the `backtesting.py` framework.
- Each strategy defines:
  - **Entry rules**: conditions for buying or shorting an asset
  - **Exit rules**: conditions for closing positions
  - **Indicators**: custom or built-in technical indicators to guide trades
- Example strategies:
  - **LongShortStrategy**: buys on upward trends, shorts on downward trends
  - **MarkovStrategy**: uses probabilities of candle streaks to predict market moves

## Data Preprocessing

- **Data Collection**: Historical OHLCV stock data is fetched using Yahoo Finance (`yfinance`).
- **Cleaning**: Remove missing values, align timestamps, and verify column consistency.
- **Preparation**: Convert raw data into the format required by the backtesting framework, including renaming columns and calculating indicators if needed.

## Backtesting

- Backtests are run using `backtesting.py`.
- Features:
  - Adjustable cash, commission, and margin
  - Ability to simulate multiple strategies on the same dataset
  - Automatic tracking of trades, returns, drawdowns, and other performance metrics

## Visualization

- Equity curves, trade entries/exits, and performance metrics are visualized using `matplotlib`.
- Helps identify strategy strengths, weaknesses, and risk exposure over time.

## Future Work

- Extend strategies with additional technical indicators (RSI, MACD, Bollinger Bands)
- Integrate machine learning-based predictions (e.g., LSTM for price forecasting)
- Implement portfolio-level backtesting with multiple assets
- Optimize strategies via parameter search or evolutionary algorithms
- Incorporate risk management techniques like position sizing and stop-loss optimization

## Tools and Libraries

- Python
- `pandas`, `numpy` for data manipulation
- `yfinance` for fetching historical stock data
- `matplotlib` for visualization
- `backtesting.py` for strategy testing

## License

This project is licensed under the [MIT License](LICENSE).

---

**Note:** This project is a work in progress. Contributions, feedback, and suggestions are welcome. Please open an issue or submit a pull request for any improvements.