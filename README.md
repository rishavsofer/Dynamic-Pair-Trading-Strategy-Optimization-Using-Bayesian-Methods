#### Overview:
This project implements a statistical arbitrage strategy using pair trading, enhanced with dynamic Z-score threshold optimization. Key steps include:
1. Identifying cointegrated stock pairs.
2. Calculating spreads with dynamic hedge ratios.
3. Generating trading signals based on Bollinger Bands and Z-scores.
4. Using Bayesian optimization to maximize the Sharpe ratio by finding optimal Z-score thresholds.
5. Backtesting the strategy with transaction costs and evaluating performance using visualizations.

---

#### Requirements:
Install the following libraries before running the script:
```bash
!pip install yfinance pandas-ta matplotlib plotly scikit-learn bayesian-optimization stable-baselines3 ipywidgets seaborn
```

---

#### Key Features:
1. **Cointegration Testing**: Ensures selected stock pairs exhibit mean-reverting behavior.
2. **Dynamic Spread Calculation**: Uses an optimized hedge ratio to model the relationship between stock pairs.
3. **Trading Signal Generation**: Based on Bollinger Bands and Z-scores for mean reversion.
4. **Bayesian Optimization**: Finds optimal Z-score thresholds for risk-adjusted return maximization.
5. **Visualizations**:
   - Heatmap of optimization results.
   - Spread with Bollinger Bands.
   - Z-score distribution.
   - Cumulative returns of the strategy.

---

#### How to Use:
1. **Load Data**: Fetch historical stock prices using `yfinance` and calculate technical indicators using `pandas-ta`.
2. **Identify Pairs**: Run cointegration tests to find tradable pairs.
3. **Optimize Parameters**: Use Bayesian optimization to dynamically identify Z-score thresholds.
4. **Backtest**: Evaluate the performance of the strategy using cumulative returns and Sharpe ratio.

---

#### Visualizations:
- **Heatmap of Optimization Results**: Identifies optimal Z-score thresholds for Sharpe ratio maximization.
- **Spread with Bollinger Bands**: Highlights key trading signals and mean-reverting behavior.
- **Z-Score Distribution**: Validates the assumption of normality in spread behavior.
- **Cumulative Returns**: Displays strategy performance over time.

---

#### Key Takeaways:
Despite observable mean-reverting patterns and optimized thresholds, the strategy demonstrated underperformance in cumulative returns. This indicates the need for:
- Refining optimization techniques.
- Incorporating alternative statistical or machine learning methods.
- Enhancing risk management to adapt to varying market conditions.
