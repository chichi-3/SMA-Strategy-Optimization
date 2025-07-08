# SMA-Strategy-Optimization
Backtesting and optimization framework for Simple Moving Average (SMA) crossover strategies. Includes in-sample and out-of-sample evaluation, strategy performance metrics (Sharpe, CAGR, drawdown), and heatmap visualization.

This project demonstrates how to backtest, evaluate, and optimize a simple moving average crossover strategy using historical market data. It walks through the full lifecycle — from initial idea to out-of-sample testing.

# Strategy Logic
Uses simple moving average (SMA) crossover:

  Buy: When shorter MA crosses above longer MA.

  Sell: When shorter MA crosses below longer MA.
