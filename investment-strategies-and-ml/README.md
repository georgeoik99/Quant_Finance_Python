# Investment Strategies and ML Classification

This project contains two complementary case studies in one notebook.

## Case study 1: Greek equity strategies

A personal universe of ten Greek-listed equities is evaluated with four transparent
approaches:

- Buy and Hold
- Monthly Equal Weight
- Inverse Volatility
- Momentum Top-2 with inverse-volatility position sizing

All strategies use the same evaluation period. Signals are executed on the next
trading day, portfolio weights are allowed to drift between rebalances, and
transaction costs are deducted. Results include CAGR, volatility, Sharpe, Sortino,
maximum drawdown, turnover, costs, equity curves, and drawdown curves.

## Case study 2: European oil-sector classification

MLP and LSTM classifiers estimate whether Repsol will exceed a **+1% return over
the following 20 trading sessions**.

The model uses the previous 20 daily returns of five economically related series:

- Repsol
- TotalEnergies
- Shell
- Eni
- iShares STOXX Europe 600 Oil & Gas UCITS ETF (EXH1)

The probability forecast is converted into a monthly Repsol-or-cash position and
then into BUY, HOLD, SELL, or CASH actions. The ML strategies are evaluated on a
chronological, purged out-of-sample test set and compared with both a classification
baseline and Repsol Buy and Hold after transaction costs.

## Run the project

```bash
python -m pip install -r requirements.txt
jupyter notebook investment_strategies_and_ml.ipynb
```

Run all cells from the top. Market data are requested from 2018 through the current
date. Local CSV caches are generated automatically as a fallback but are not stored
in this repository.

## Methodological notes

- No Markowitz/minimum-variance optimizer is used.
- Scalers are fitted only on training data.
- Training, validation, and test samples are separated chronologically.
- Purge gaps match the 20-day forecast horizon to reduce leakage.
- A complex model is considered useful only if it improves relevant out-of-sample
  and investment benchmarks.

## Limitations

The projects use a small selected universe, fixed transaction costs, and publicly
available market data. Taxes, time-varying bid-ask spreads, market impact, and
point-in-time universe membership are outside the scope of the analysis.

> Educational research only. The outputs are not investment recommendations.

