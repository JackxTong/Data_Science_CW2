# Data Science Coursework2

This project is submitted as CW2 to MATH 70076 Data Science at Imperial College London. This is aimed to be an open-source and reproducible data science project, featuring how we can fetch historical stock data of AAPL using data pipeline of, and do data analysis on my personal webpage using the template of [Jupyter-book](https://jupyterbook.org/en/stable/start/your-first-book.html)

The website is hosted [here](https://jackxtong.github.io/Data_Science_CW2/), and published online with Github Pages.

## To use Jupyter-Book:

Clone my repository, or follow the instructions at [Jupyter-book](https://jupyterbook.org/en/stable/start/your-first-book.html). 

You can create a venv, then activate the venv, and install all dependencies:

```bash
python3 -m pip install -r requirements.txt`
```

Then simply put your jupyter notebooks at root directoy, make sure you add them to the `_toc.yml` file, and specify the upstream at `_config.yml`.  
Building the book locally:

```bash
jb build .
```

Hosting it online (by pushing to gh-pages branch at your github)
```bash
pip install ghp-import
ghp-import -n -p -f _build/html
```

## Functionalities

### Fetching and analyzing stock data
The first notebook fetched historical AAPL stock data using free yfinance API. It studies the time series properties of AAPL stock series, analyzing whether it displays the four stylized facts for financial time series.

### Fetching and analyzing options data
The second notebook uses data pipeline of [market data](https://api.marketdata.app/v1/options/chain/AAPL/). It studies the distribution of the call options data of AAPL, analyzing whether it agrees with Black-Scholes framework.