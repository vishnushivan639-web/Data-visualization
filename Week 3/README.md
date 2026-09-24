# Apple Stock Analysis

## 📌 Project Overview

This project performs an exploratory analysis of **Apple Inc. (AAPL) stock data** using Python. The analysis focuses on understanding historical stock prices, trading volume, daily price changes, returns, and unusual trading activity.

The project uses a dataset containing Apple stock information from **September 2014 to March 2018**.

---

## 🎯 Objectives

The main objectives of this project are:

* Analyze historical Apple stock price data.
* Understand the Open, High, Low, Close, and Adjusted Close prices.
* Analyze trading volume.
* Calculate daily price changes.
* Calculate daily returns.
* Identify high-volume/anomalous trading days.
* Calculate statistical measures such as mean, variance, and standard deviation.
* Identify the highest-volume trading days.

---

## 📂 Dataset

The project uses an Excel dataset named:

`AAPL.xlsx`

### Dataset Features

| Column    | Description                     |
| --------- | ------------------------------- |
| Date      | Trading date                    |
| Open      | Opening stock price             |
| High      | Highest price during the period |
| Low       | Lowest price during the period  |
| Close     | Closing stock price             |
| Adj Close | Adjusted closing price          |
| Volume    | Trading volume                  |

### Dataset Size

* **Rows:** 184
* **Columns:** 7
* **Time Period:** September 2014 – March 2018

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook / Google Colab
* Microsoft Excel dataset

---

## 🔄 Project Workflow

### 1. Import Libraries

The project uses the following Python libraries:

* `pandas` for data manipulation
* `numpy` for numerical operations
* `matplotlib` for visualization
* `seaborn` for visualization

### 2. Load Dataset

The AAPL stock dataset is loaded using Pandas:

```python
df = pd.read_excel("AAPL.xlsx")
```

### 3. Data Exploration

The project examines:

* First few records
* Last few records
* Dataset shape
* Data types
* Statistical summary
* Missing values

### 4. Data Cleaning

The following preprocessing operations are performed:

* Missing values are checked.
* Missing records are removed using `dropna()`.
* Duplicate records are removed using `drop_duplicates()`.
* Data is sorted according to the `Date` column.

### 5. Feature Engineering

Two additional features are calculated.

#### Daily Delta

```python
Daily_Delta = Close - Open
```

This represents the difference between the closing and opening prices.

#### Daily Return

```python
Daily_Return = ((Close - Open) / Open) * 100
```

This represents the percentage change between the opening and closing prices.

---

## 📊 Statistical Analysis

The project calculates the average, maximum, and minimum values for the Open and Close prices.

### Average

* Average Open Price: **127.04**
* Average Close Price: **127.35**

### Maximum

* Maximum Open Price: **180.29**
* Maximum Close Price: **179.98**

### Minimum

* Minimum Open Price: **92.39**
* Minimum Close Price: **90.52**

---

## 📈 Return Analysis

The project calculates statistical measures for daily returns.

| Measure            |   Value |
| ------------------ | ------: |
| Mean Return        | 0.3072% |
| Variance           | 12.2892 |
| Standard Deviation | 3.5056% |

The mean daily return calculated from the dataset is approximately **0.31%**.

---

## 📦 Trading Volume Analysis

The project also analyzes the trading volume.

| Measure        |       Value |
| -------------- | ----------: |
| Average Volume | 191,016,776 |
| Minimum Volume |  38,398,505 |
| Maximum Volume | 500,363,000 |

The highest recorded trading volume in the dataset is **500,363,000**.

---

## 🚨 Anomalous Trading Days

The analysis identifies high-volume trading days based on the project's volume threshold.

The identified high-volume dates include:

* **2015-01-26**
* **2015-04-27**
* **2015-08-03**
* **2015-08-24**
* **2016-09-12**

Among these, **2015-08-24** has the highest volume at **500,363,000** and a calculated daily return of approximately **19.42%**.

---

## 🔝 Top Volume Days

The project sorts the dataset by trading volume in descending order and extracts the **top 10 highest-volume trading days**.

This helps identify periods when Apple stock experienced unusually high market activity.

---

## 🔍 Key Findings

Based on the analysis performed in the notebook:

* The dataset contains **184 records** and **7 original features**.
* No missing values were present in the original dataset.
* The average closing price was approximately **127.35**.
* The maximum closing price was approximately **179.98**.
* The minimum closing price was approximately **90.52**.
* Average trading volume was approximately **191 million**.
* The maximum trading volume was **500.36 million**.
* The calculated mean daily return was approximately **0.31%**.
* Several high-volume trading periods were identified for further analysis.

---

## ▶️ How to Run the Project

### Using Google Colab

1. Open the notebook in Google Colab.
2. Upload the `AAPL.xlsx` dataset.
3. Make sure the dataset path matches the path used in the notebook.
4. Run the notebook cells sequentially.

### Using Jupyter Notebook

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn openpyxl
```

Then open the notebook:

```bash
jupyter notebook "Apple stock.ipynb"
```

Place `AAPL.xlsx` in the appropriate project directory and run the cells sequentially.

---

## 📁 Project Structure

```text
Apple-Stock-Analysis/
│
├── Apple stock.ipynb
├── AAPL.xlsx
└── README.md
```

---

## 📌 Conclusion

This project provides an exploratory analysis of historical Apple stock data. It demonstrates the use of Python and Pandas for data loading, cleaning, feature engineering, statistical analysis, and identification of high-volume trading periods.

The analysis can be further extended by adding stock-price visualizations, moving averages, correlation analysis, volatility analysis, and predictive machine-learning models.

---

## 👨‍💻 Project Type

**Data Analysis / Exploratory Data Analysis (EDA)**

**Dataset:** Apple Inc. (AAPL) Historical Stock Data
