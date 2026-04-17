# 📈 Pandas Mini Project — Statistics from Stock Data

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C)

## 🚀 Overview

A Pandas data analysis exercise that loads historical stock data for Google, Apple, and Amazon (2000–2016) from CSV files, joins them into a unified DataFrame indexed by calendar date, computes descriptive statistics (mean, median, standard deviation, correlation matrix), and visualizes rolling mean (150-day moving average) for trend analysis.

## ✨ What It Covers

- **CSV Loading with Parsing** — `pd.read_csv()` with `index_col`, `parse_dates`, and `usecols` to load only the `Date` and `Adj Close` columns with datetime indexing
- **DataFrame Joining** — Creating a date-range indexed DataFrame (`pd.date_range('2000-01-01', '2016-12-31')`) and joining three stock DataFrames with renamed columns for unique labels
- **NaN Handling** — Detecting missing values with `.isnull()` and removing rows with `.dropna()` (calendar dates without trading data)
- **Descriptive Statistics** — `.mean()`, `.median()`, `.std()` per stock, and `.corr()` for the cross-stock correlation matrix
- **Rolling Statistics** — 150-day rolling mean (moving average) computed with `.rolling(150).mean()` and plotted against raw price data
- **Visualization** — Matplotlib line plot overlaying Google stock price with its 150-day moving average

## 📊 Dataset

| File | Stock | Records | Date Range |
|---|---|---|---|
| `GOOG.csv` | Google | 3,313 | 2004–2016 |
| `AAPL.csv` | Apple | 4,475 | 2000–2016 |
| `AMZN.csv` | Amazon | 4,475 | 2000–2016 |

Source: Yahoo Finance. Columns: Date, Open, High, Low, Close, Adj Close, Volume.

## 🛠 Tech Stack

| Component | Technology |
|---|---|
| Language | Python |
| Data Analysis | Pandas |
| Visualization | Matplotlib |
| Environment | Jupyter Notebook |

## ⚡ Getting Started

```bash
git clone https://github.com/jashjain21/Pandas-mini_project.git
cd Pandas-mini_project

pip install pandas matplotlib

jupyter notebook "Statistics from Stock Data.ipynb"
```

## 🔍 What This Project Demonstrates

- **Pandas Data Wrangling** — CSV parsing, datetime indexing, column renaming, DataFrame joining, and NaN handling
- **Exploratory Data Analysis** — Computing and interpreting descriptive statistics and correlation matrices across multiple time series
- **Time Series Analysis** — Rolling window statistics for smoothing noisy stock price data and identifying trends
