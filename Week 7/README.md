# 📊 Student Performance Analysis

## 📌 Project Overview

This project analyzes student performance using Python and the **Student Performance Dataset**.

The analysis focuses on understanding students' scores in **Math, Reading, and Writing** and performing basic statistical analysis to identify overall performance, score distribution, and potential outliers.

---

## 🎯 Objectives

The main objectives of this project are:

* Analyze student performance in different subjects.
* Understand the structure and characteristics of the dataset.
* Calculate descriptive statistics.
* Find the mean, median, and standard deviation of scores.
* Calculate the total score for each student.
* Calculate the percentage scored by each student.
* Identify potential outliers in subject scores.

---

## 📂 Dataset

The dataset contains **1000 student records** and **8 columns**.

### Dataset Features

| Column                        | Description                    |
| ----------------------------- | ------------------------------ |
| `gender`                      | Gender of the student          |
| `race/ethnicity`              | Race/ethnicity group           |
| `parental level of education` | Parent's education level       |
| `lunch`                       | Type of lunch received         |
| `test preparation course`     | Test preparation course status |
| `math score`                  | Mathematics score              |
| `reading score`               | Reading score                  |
| `writing score`               | Writing score                  |

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** – Data manipulation and analysis
* **NumPy** – Numerical operations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Google Colab / Jupyter Notebook**

---

## 🔍 Project Workflow

### 1. Import Libraries

The project uses:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

### 2. Load Dataset

The dataset is loaded using Pandas:

```python
df = pd.read_csv("/content/sample_data/archive (13).zip")
```

### 3. Explore the Dataset

The project examines the dataset using:

```python
df.info()
df.head()
df.tail()
df.describe()
df.columns
```

These operations help understand the dataset structure, columns, records, and numerical statistics.

### 4. Check Missing Values

Missing values are checked using:

```python
df.isnull().sum()
```

### 5. Statistical Analysis

The three score columns are selected:

```python
score_columns = ['math score', 'reading score', 'writing score']
```

The project calculates:

* Mean
* Median
* Standard deviation
* Quartiles

Example:

```python
df[score_columns].mean()
df[score_columns].median()
df[score_columns].std()
```

### 6. Calculate Total Score

A new column called `Total Score` is created:

```python
df["Total Score"] = (
    df["math score"] +
    df["reading score"] +
    df["writing score"]
)
```

The total is calculated out of **300**.

### 7. Calculate Percentage

The percentage is calculated using:

```python
df["Percentage"] = (df["Total Score"] / 300) * 100
```

### 8. Outlier Detection

The project uses the **Interquartile Range (IQR)** method to identify potential outliers in:

* Math score
* Reading score
* Writing score

The calculation uses:

```text
IQR = Q3 - Q1

Lower Limit = Q1 - 1.5 × IQR

Upper Limit = Q3 + 1.5 × IQR
```

Scores outside these limits are identified as potential outliers.

---

## 📈 Statistical Summary

The notebook calculates descriptive statistics for all three subjects.

| Subject |   Mean | Median | Standard Deviation |
| ------- | -----: | -----: | -----------------: |
| Math    | 66.089 |     66 |             15.163 |
| Reading | 69.169 |     70 |             14.600 |
| Writing | 68.054 |     69 |             15.196 |

The dataset contains **1000 student records**.

---

## 💡 Key Analysis Areas

This project provides analysis of:

1. Dataset structure
2. Missing values
3. Subject-wise score statistics
4. Mean and median scores
5. Score variability
6. Total student scores
7. Student percentages
8. Score quartiles
9. Potential outliers

---

## 🚀 How to Run the Project

### Step 1: Clone the Repository

```bash
git clone <your-repository-url>
```

### Step 2: Open the Notebook

Open:

```text
student performance.ipynb
```

using **Jupyter Notebook** or **Google Colab**.

### Step 3: Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn
```

### Step 4: Run the Notebook

Run the cells sequentially to reproduce the analysis.

---

## 📁 Project Structure

```text
Student-Performance-Analysis/
│
├── student performance.ipynb
├── README.md
└── dataset/
    └── student performance dataset
```

---

## 🔮 Future Improvements

The project can be extended by adding:

* Gender-wise performance analysis
* Performance comparison based on parental education
* Test preparation course analysis
* Lunch category performance analysis
* Correlation analysis between subjects
* Data visualization using charts
* Student performance classification
* Machine learning models for performance prediction

---

## 👨‍💻 Project Type

**Data Analysis / Exploratory Data Analysis (EDA)**

---

## 📜 License

This project is created for educational and learning purposes.
