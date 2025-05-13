# 📊 Data Science Coursework 2 — Imperial College London

This repository contains the final project for **MATH 70076: Data Science** at **Imperial College London**. The project is designed to be **open-source, reproducible**, and demonstrates the application of data pipelines and exploratory data analysis in **financial data science**.

The goal is to showcase how to:

- Fetch and analyze **historical stock data** using the `yfinance` API.
- Fetch and analyze **options data** using the `Market Data` public API.
- Present the analysis through a clean and interactive **Jupyter Book**.
- Host the analysis online via **GitHub Pages**.

📚 **Website**: [https://jackxtong.github.io/Data_Science_CW2/](https://jackxtong.github.io/Data_Science_CW2/)

---

## 📁 Project Structure

```text
├── _build/              # Output folder for the compiled Jupyter Book
├── _config.yml          # Jupyter Book configuration
├── _toc.yml             # Table of contents for the Jupyter Book
├── data_analysis/       # Jupyter notebooks for exploring and analyzing data
├── intro.md             # Introduction chapter for the Jupyter Book
├── logo.png             # Logo used in the book or documentation
├── option_data/         # Raw or processed option data used in analysis
├── pipeline/            # Introduction to the usage of pipelines
├── references.bib       # Bibliographic references for citations in the book
├── requirements.txt     # Python dependencies
├── scripts/             # Utility scripts for data preparation
└── README.md            # Project overview (this file)
```

## Book structure

First chapter "Intro to Data Pipelines used" in `pipeline/` introduces how to use the two API.  
Second chapter "Data analysis" in `data_analysis/` contains the two notebooks using the two APIs for data analysis on the stock and options data of Apple Inc.

## 🚀 Getting Started

To build and view the Jupyter Book locally:

### 1. Clone the Repository

```bash
git clone https://github.com/jackxtong/Data_Science_CW2.git
cd Data_Science_CW2
```

### 2. Create a Virtual Environment and Install Dependencies

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### 3. Add jupyter notebooks into root
- Add them to `_toc.yml` to include them in the book
- Edit `_config.yml` to set the upstream

### 4. Build the book

```bash
jb build .
```

### 5. Host the Book on Github Pages

Install the tool, then push the compiled book to the gh-pages branch:
```bash
pip install ghp-import
ghp-import -n -p -f _build/html
```

## 📈 Functionalities & Analysis

### 1. Historical Stock Data Analysis

- Fetches historical stock data for **AAPL (Apple Inc.)** using the `yfinance` API
- Performs exploratory time series analysis on both price levels and returns
- Investigates classic **stylized facts** of financial time series:
  - Volatility clustering
  - Heavy tails
  - Absence of autocorrelation in returns
  - Leverage effects

📓 Notebook: `data_analysis/Aapl_stock.ipynb`

---

### 2. Options Market Analysis

- Uses the [Market Data API](https://api.marketdata.app/v1/options/chain/AAPL/) to retrieve **AAPL call options** data
- Analyzes the distribution of option prices across strike and expiry dimensions
- Compares empirical observations with assumptions of the **Black-Scholes model**, including:
  - Log-normality of returns
  - Constant volatility

📓 Notebook: `data_analysis/Aapl_options.ipynb`
