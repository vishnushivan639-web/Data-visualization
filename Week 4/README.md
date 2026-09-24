# Shopify Stock Analysis

## 📌 Project Overview

This project performs an exploratory analysis of **Shopify Inc. (SHOP) stock data** using Python.

The analysis focuses on understanding Shopify's historical closing prices, price trends, moving averages, and daily returns through data visualization and statistical exploration.

The dataset contains Shopify stock information from **May 2015 to March 2025**.

---

## 🎯 Objectives

The main objectives of this project are:

* Analyze Shopify's historical stock prices.
* Visualize the closing price over time.
* Calculate and visualize **20-day and 50-day Simple Moving Averages (SMA)**.
* Calculate daily stock returns.
* Analyze the distribution of daily returns.
* Visualize daily-return frequency using a histogram.
* Visualize the probability distribution of daily returns using KDE.

---

## 📂 Dataset

The project uses a CSV dataset named:

`shopify_stock.csv`

### Dataset Features

| Column      | Description                                |
| ----------- | ------------------------------------------ |
| `date`      | Trading date                               |
| `open`      | Opening stock price                        |
| `high`      | Highest stock price during the trading day |
| `low`       | Lowest stock price during the trading day  |
| `close`     | Closing stock price                        |
| `adj_close` | Adjusted closing price                     |
| `volume`    | Number of shares traded                    |

### Dataset Information

* **Rows:** 2,469
* **Columns:** 7
* **Start Date:** May 21, 2015
* **End Date:** March 14, 2025

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook / Google Colab

---

## 🔄 Project Workflow

### 1. Import Libraries

The project uses Python libraries for data manipulation and visualization:

```python
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
import seaborn as sns
```

### 2. Load the Dataset

The Shopify stock CSV file is loaded using Pandas:

```python
df = pd.read_csv("/content/sample_data/shopify_stock.csv")
```

### 3. Explore the Dataset

The project displays the dataset and its first few records to understand the available stock information.

```python
df
```

and:

```python
df.head()
```

### 4. Convert Date Column

The `date` column is converted into a Pandas datetime format:

```python
df['date'] = pd.to_datetime(df['date'], utc=True)
```

This allows the stock data to be analyzed and visualized according to time.

---

## 📈 Closing Price Analysis

A line chart is created to visualize Shopify's **closing price over time**.

The visualization contains:

* Date on the X-axis
* Closing price on the Y-axis
* Historical Shopify closing-price movement

This provides a visual representation of how Shopify's stock price changed throughout the dataset period.

---

## 📊 Moving Average Analysis

Two Simple Moving Averages are calculated:

### 20-Day SMA

```python
df['SMA_20'] = df['close'].rolling(window=20).mean()
```

### 50-Day SMA

```python
df['SMA_50'] = df['close'].rolling(window=50).mean()
```

The closing price is plotted together with the 20-day and 50-day moving averages.

Moving averages are used in this project to provide smoothed representations of the historical closing-price series.

---

## 📉 Daily Return Analysis

Daily returns are calculated using the percentage change in the closing price:

```python
df['Daily_Return'] = df['close'].pct_change() * 100
```

The first record is removed from the return analysis because a previous closing price is required to calculate the percentage change.

```python
df_returns = df.dropna(subset=['Daily_Return'])
```

---

## 📊 Daily Return Histogram

A histogram is created to visualize the distribution of Shopify's daily returns.

```python
sns.histplot(df_returns['Daily_Return'], bins=50, kde=False)
```

The histogram helps examine how frequently different daily-return values occur within the dataset.

---

## 📈 Daily Return KDE

A Kernel Density Estimate (KDE) plot is also created:

```python
sns.kdeplot(df_returns['Daily_Return'], fill=True)
```

The KDE provides a smoothed view of the distribution of daily stock returns.

---

## 🔍 Key Analysis Performed

The notebook includes the following analyses:

* Historical closing-price visualization
* 20-day Simple Moving Average
* 50-day Simple Moving Average
* Daily percentage return calculation
* Daily return histogram
* Daily return KDE distribution

---

## 📁 Project Structure

```text
Shopify-Stock-Analysis/
│
├── shopify stock.ipynb
├── shopify_stock.csv
└── README.md
```

---

## ▶️ How to Run the Project

### Using Google Colab

1. Open `shopify stock.ipynb` in Google Colab.
2. Upload `shopify_stock.csv`.
3. Make sure the CSV file is available at the path used in the notebook.
4. Run the notebook cells sequentially.

### Using Jupyter Notebook

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

Then open the notebook:

```bash
jupyter notebook "shopify stock.ipynb"
```

Place `shopify_stock.csv` in the appropriate directory and execute the notebook cells.

---

## 📌 Conclusion

This project provides an exploratory analysis of Shopify historical stock data using Python.

It demonstrates how stock-price data can be loaded, processed, visualized, and analyzed using **Pandas, Matplotlib, and Seaborn**. The project specifically examines closing-price trends, moving averages, and the distribution of daily stock returns.

---

## 👨‍💻 Project Type

**Data Analysis / Exploratory Data Analysis (EDA)**

**Dataset:** Shopify Inc. (SHOP) Historical Stock Data
