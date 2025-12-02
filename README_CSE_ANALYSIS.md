# Colombo Stock Exchange (CSE) Stock Market Analysis

A comprehensive Python Jupyter notebook for analyzing stocks listed on the Colombo Stock Exchange (CSE).

## Features

- **Data Fetching**: Retrieve historical stock data from Yahoo Finance (CSE stocks use `.CM` suffix)
- **Technical Analysis**: Calculate popular indicators including:
  - Simple Moving Average (SMA)
  - Exponential Moving Average (EMA)
  - Relative Strength Index (RSI)
  - Moving Average Convergence Divergence (MACD)
  - Bollinger Bands
  - Average True Range (ATR)
  - Stochastic Oscillator
- **Visualization**: Interactive and static charts for price movements and indicators
- **Portfolio Management**: Track and analyze your investment portfolio
- **Trading Signals**: Generate buy/sell signals based on technical indicators
- **Stock Screening**: Compare and screen multiple stocks

## Installation

1. Clone or download this repository
2. Install Python 3.8 or higher
3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Launch Jupyter Notebook:

```bash
jupyter notebook cse_stock_analysis.ipynb
```

## Quick Start

```python
# 1. Fetch stock data
data = fetch_stock_data('JKH.CM', period='1y')

# 2. Add technical indicators
data_with_indicators = add_all_indicators(data.copy())

# 3. Visualize
plot_candlestick(data, title="JKH Candlestick")
plot_with_indicators(data_with_indicators, ticker="JKH.CM")

# 4. Get trading signals
signals = get_signal_summary(data_with_indicators)

# 5. Track portfolio
portfolio = Portfolio()
portfolio.add_holding('JKH.CM', 100, 150.00)
portfolio.get_summary()
```

## Available CSE Stocks

The notebook includes common CSE stock tickers:

| Ticker | Company |
|--------|---------|
| JKH.CM | John Keells Holdings |
| COMB.CM | Commercial Bank of Ceylon |
| SAMP.CM | Sampath Bank |
| HNB.CM | Hatton National Bank |
| DIAL.CM | Dialog Axiata |
| SLTL.CM | Sri Lanka Telecom |
| HPFL.CM | Hayleys PLC |
| CARG.CM | Cargills Ceylon |
| ...and more |

## Data Sources

1. **Yahoo Finance** - Primary source (limited CSE coverage)
2. **Manual Entry** - Support for CSV import and manual data entry
3. **CSE Official Website** - https://www.cse.lk/

## Important Notes

- CSE trading hours: 9:30 AM - 2:30 PM (Sri Lanka Standard Time)
- Market is closed on weekends and Sri Lankan public holidays
- Price quotes are in Sri Lankan Rupees (LKR)
- Not all CSE stocks may be available on Yahoo Finance

## Disclaimer

**This notebook is for educational and personal analysis purposes only. It does not constitute financial advice. Always do your own research and consult with a qualified financial advisor before making investment decisions.**

## License

This project is for personal use.
