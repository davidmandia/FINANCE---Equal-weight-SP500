# Equal-Weight S&P 500 Index Fund

## Overview

The S&P 500 is the world's most popular stock market index. The largest fund that is benchmarked to this index is the SPDR® S&P 500® ETF Trust, which has more than US$250 billion of assets under management.

The goal of this Python script is to create a tool that accepts the value of a portfolio and recommends how many shares of each S&P 500 constituent should be purchased to create an equal-weight version of the index fund.

## Library Imports

The script uses several Python libraries:
- `numpy` for numerical operations.
- `pandas` for data manipulation and analysis.
- `requests` for making HTTP requests to the IEX Cloud API.
- `xslxwriter` for writing Excel files.
- `math` for mathematical operations.

## Usage

1. **Import List of Stocks**: The script imports a list of S&P 500 stocks from a CSV file named `sp_500_stocks.csv`.

2. **Acquiring an API Token**: It requires an API token from IEX Cloud for data retrieval. The token should be stored securely in a `secrets.py` file in the same directory as the script.

3. **API Calls**: The script makes API calls to fetch the latest stock prices and market capitalizations for each stock.

4. **Calculating Shares to Buy**: Based on the portfolio size provided by the user, the script calculates the number of shares to buy for each stock to achieve an equal-weight portfolio.

5. **Excel Output**: The recommendations are saved into an Excel file named `recommended_trades.xlsx` in the same directory.

## Note

- The script requires a valid API token from IEX Cloud to function properly.
- Make sure to replace `'your_actual_api_token_here'` in the `secrets.py` file with your real API token.

