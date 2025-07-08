#  Moving Average Crossover Strategy (Backtest & Optimization)
Backtesting and optimization framework for Simple Moving Average (SMA) crossover strategies. Includes in-sample and out-of-sample evaluation, strategy performance metrics (Sharpe, CAGR, drawdown), and heatmap visualization.

This project demonstrates how to backtest, evaluate, and optimize a simple moving average crossover strategy using historical market data. It walks through the full lifecycle — from initial idea to out-of-sample testing.

## Strategy Logic

- Simple moving average crossover.
- **Buy signal**: Short MA crosses above Long MA.
- **Sell signal**: Short MA crosses below Long MA.

###  1. Exploratory Data Analysis (EDA)
- Quick overview of data to confirm structure and availability.
- Initial plot of price data.

###  2. Backtest: 50/200 SMA (Golden & Death Cross)
- Benchmarked the strategy using the classic 50/200 pair.
- Chosen due to its popularity in traditional technical analysis.

###  3. Backtest Performance Evaluation
- Equity curves plotted for:
  - Strategy
  - Long-only
  - Short-only
  - Buy & Hold
- Metrics calculated:
  - Net profit, CAGR, Sharpe Ratio, Max Drawdown
  - Gross profit/loss, Avg trade return, Largest win/loss
  - Profit factor, percent profitable

###  4. MA Optimization
- Grid of moving average values used:[3, 5, 8, 10, 13, 15, 20, 25, 30, 35, 40, 45, 50, 60,
75, 100, 125, 150, 175, 200, 250, 300]
- All valid short < long MA combinations tested.
- Evaluation metrics stored and visualized using heatmaps.

###  5. Out-of-Sample Evaluation
- Data was split into in-sample and out-of-sample periods.
- Best-performing MA pair on training set was tested on unseen data.
- Same metrics recalculated for validation.

##  Conclusion

This moving average crossover strategy is **not suitable for real-world trading** as-is.

- The full strategy underperforms Buy & Hold.
- Even after optimization, it suffers from poor drawdowns and overfitting risks.
- **However**, the exercise is valuable to:
- Understand how strategy building works.
- Learn the importance of validation and risk metrics.
- Filter out curve-fitted strategies through proper backtesting.
