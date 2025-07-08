#  Moving Average Crossover Strategy (Backtest & Optimization)
Backtesting and optimization framework for Simple Moving Average (SMA) crossover strategies. Includes in-sample and out-of-sample evaluation, strategy performance metrics (Sharpe, CAGR, drawdown), and heatmap visualization.

This project demonstrates how to backtest, evaluate, and optimize a simple moving average crossover strategy using historical market data. It walks through the full lifecycle from initial idea to out-of-sample testing.

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

We were able to find a moving average pair that performed better than the initial 50/200 strategy. However, both the original and the optimized versions underperformed Buy & Hold.

There was also a noticeable difference between in-sample and out-of-sample returns, highlighting the risk of overfitting. This shows why relying only on backtest performance can be misleading, proper validation is key.

Overall, this project serves as a strong example of how to approach strategy development carefully, not just to find what works, but also to understand what doesn’t.

### Important Note

This strategy was evaluated without any risk management techniques, such as stop-loss placement, position sizing, or capital allocation rules. These factors play a critical role in real-world trading performance. While the current results underperform Buy & Hold, the strategy may hold potential if enhanced with proper risk controls and money management practices.
