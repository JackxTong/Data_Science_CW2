# Data Science Coursework2

This project is submitted as CW2 to MATH 70076 Data Science at Imperial College London. This is aimed to be an open-source and reproducible data science project, featuring how we can fetch historical stock data of AAPL using data pipeline of, and do data analysis on my personal webpage using the template of [Jupyter-book](https://jupyterbook.org/en/stable/start/your-first-book.html)

## Functionalities

### Fetching and analyzing stock data
data pipeline is yfinance

### Fetching and analyzing options data
data pipeline is [market data](https://api.marketdata.app/v1/options/chain/AAPL/)

Need to create an account there, get its API token, store in an `.env` file with `MARKETDATA_API_KEY = REZXXXX`.