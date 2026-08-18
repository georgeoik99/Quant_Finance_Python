# Quantitative Finance with Python

This repository is a collection of small, reproducible projects in quantitative
finance. It focuses on portfolio construction, transparent backtesting, risk and
performance measurement, and the careful use of machine learning for trading
signals.

The goal is not to present complex models as automatically superior. Each project
starts with a financial question, defines an investable benchmark, accounts for
timing and transaction costs, and interprets the results in economic terms.

## Projects

| Project | Topics |
| --- | --- |
| [Portfolio Allocation Rules](projects/portfolio-allocation-rules/) | Equal-weight and inverse-volatility portfolios compared with the S&P 500 |
| [Investment Strategies and ML Classification](projects/investment-strategies-and-ml/) | Greek equity strategies and MLP/LSTM classification for Repsol using European oil-sector data |

## Repository structure

```text
Quant_Finance_Python/
├── README.md
└── projects/
    ├── portfolio-allocation-rules/
    │   ├── README.md
    │   └── portfolio_optimization.ipynb
    └── investment-strategies-and-ml/
        ├── README.md
        ├── investment_strategies_and_ml.ipynb
        └── requirements.txt
```

Each project folder contains its own short README with the research question,
methodology, data, and instructions for running the notebook.

## Main tools

- Python and Jupyter
- pandas, NumPy, Matplotlib
- yfinance
- scikit-learn
- TensorFlow/Keras

## Notes

- Market data are downloaded at notebook runtime, so results may change as new
  observations become available or data providers revise historical series.
- The notebooks are educational research projects, not investment advice.
- Historical and out-of-sample performance does not guarantee future results.

