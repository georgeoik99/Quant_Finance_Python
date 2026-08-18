# Portfolio Allocation Rules

This mini-project compares two simple, non-optimization portfolio allocation
rules with an S&P 500 benchmark.

## Strategies

- **Equal Weight:** allocates the same weight to every asset.
- **Inverse Volatility:** assigns larger weights to assets with lower recent
  volatility.
- **Benchmark:** S&P 500 buy-and-hold exposure.

The notebook applies monthly rebalancing and evaluates the strategies with CAGR,
annualized volatility, Sharpe ratio, and maximum drawdown.

## Asset universe

The sample combines US equities from several sectors with Viohalco, gold exposure,
and a long-duration US Treasury ETF. It is intended to demonstrate diversification
and rule-based portfolio construction rather than estimate an optimal Markowitz
portfolio.

## Notebook

Open and run [`portfolio_optimization.ipynb`](portfolio_optimization.ipynb).
The notebook downloads market data with `yfinance`, constructs the portfolios,
plots their equity curves, and reports the performance metrics.

> Educational example only. Historical performance is not investment advice.

