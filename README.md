# Cointegration-Based Pairs Trading Strategy
## Overview
This project develops and evaluates a statistical arbitrage strategy on U.S. financial equities using Python.
The strategy screens candidate pairs using return correlation and the Engle-Granger cointegration test, estimate hedge ratios using OLS regression, and evaluates mean-reversion trading signals out-of-sample.
## Methodology
1.Download daily adjusted equity prices.
2.Split the data into training and testing periods.
3.Calculate daily return correlations.
4.Apply Engle-Granger cointegration tests to identify candidate pairs.
5.Estimate the hedge ratio using OLS regression on training data.
6.Construct the spread and z-score.
7.Generate mean-reversion trading signals. 
8.Backtest the strategy out-of-sample.
9.Include 5 bps transaction costs.
10.Perform parameter sensitivity analysis.
## Selected Pair
BAC-PNC
Training-period statistcs:
- Return correlation: approximately 0.807
- Cointegration p-value: approximately 0.041
- Hedge ratio: approximately 4.108
## Trading Rules
- Long the spread when z-score < -2
- Short the spread when z-score > 2
- Exit when |z-score| < 0.5
## Results
Using a 2-standard-deviation entry threshold:
- Out of-sample cumulative return: approximately 5.2%
- Annualized Sharpe ratio after 5 bps transaction costs: approximately 0.52
Sensitivity analysis across entry thresholds of 1.5, 2.0 and 2.5 produced positive Sharpe ratios.
## Limitations
- Small equity universe
- Limited number of trades
- Static hedge ratio
- Simplified transaction-cost assumptions
- Cointegration relationships may break across market regimes




