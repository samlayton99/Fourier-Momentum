# Quasi-Momentum Trading Strategies Using Fourier Transforms

## Overview

This repository contains an implementation of momentum and quasi-momentum trading strategies using the Fast Fourier Transform (FFT) for signal processing of equity price data. The project demonstrates how FFT techniques can be applied to traditional momentum strategies to potentially reduce volatility while maintaining similar returns.

## Key Features

- Implementation of three distinct momentum strategies:
  - **Traditional Momentum** (Benchmark)
  - **Rolling FFT Momentum** (Signal processing approach)
  - **Continuity-Adjusted Momentum** (Volatility-aware approach)
- Comprehensive portfolio performance analysis and factor model testing
- Visualization tools for comparing strategy performance
- Signal processing techniques applied to financial time series

## Methodology

The project explores how signal processing techniques can address common issues in rolling calculations, such as sudden spikes and drops when anomalies enter or leave the rolling window. The implemented strategies are:

1. **Benchmark Momentum**: Traditional approach using summation of log-adjusted returns from t-12 to t-2 months
2. **Rolling FFT Momentum**: Extracts general trends by applying Fourier Transform to price data, keeping only low-frequency components
3. **Continuity-Adjusted Momentum**: Extends the FFT approach by weighting momentum values based on a discontinuity score (MSE between actual and FFT-cleaned prices)

## Key Findings

- The quasi-momentum strategies demonstrate similar returns to the benchmark strategy
- Continuity-Adjusted Momentum shows significantly lower volatility in spread portfolios
- Improved Sharpe ratios for the Continuity-Adjusted approach due to reduced volatility
- Traditional factors (market beta, HML, SMB) explain excess returns similarly across all strategies
- Potential reduction in drawdowns during volatile market periods

## Technologies Used

- **Python** for implementation and analysis
- **NumPy** and **Pandas** for data manipulation
- **SciPy** for Fast Fourier Transform calculations
- **Matplotlib** for visualization
- **StatsModels** for regression analysis and factor testing

## Data Sources

- Monthly US equity data from CRSP (NYSE, AMEX, and Nasdaq)
- Factor data from Ken French's website
- Backtest period: 1962-08-01 to 2022-09-01

## Usage

The implementation is provided in the Jupyter notebook `portfolios.ipynb`, which contains:
- Data preparation and parameter selection
- Strategy implementation functions
- Performance evaluation and visualization tools
- Factor model testing

## Applications

This research demonstrates practical applications of signal processing techniques in quantitative finance and may be relevant for:
- Quantitative trading firms seeking to reduce portfolio volatility
- Asset managers looking to improve existing momentum strategies
- Researchers exploring new approaches to mitigate momentum crashes

---
