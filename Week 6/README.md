# Healthcare Data Analysis

## 📌 Project Overview

This project performs an exploratory analysis of a **Healthcare Dataset** using Python.

The analysis focuses on understanding patient information, medical conditions, billing amounts, insurance providers, admission patterns, and the relationship between age and billing amount.

The project uses **Pandas, Matplotlib, and Seaborn** for data loading, data analysis, statistical analysis, and visualization.

---

## 🎯 Objectives

The main objectives of this project are:

* Explore the healthcare dataset and its structure.
* Understand the numerical and categorical variables.
* Check for missing values.
* Analyze admission trends over time.
* Identify the month with the highest number of admissions.
* Compare total billing amounts across medical conditions and insurance providers.
* Analyze billing amount distributions.
* Calculate average billing amounts by medical condition.
* Calculate average billing amounts by insurance provider.
* Analyze monthly admission patterns.
* Study the correlation between patient age and billing amount.

---

## 📂 Dataset

The project uses a healthcare dataset named:

`healthcare_dataset (1).csv`

### Dataset Size

* **Rows:** 55,500
* **Columns:** 15

### Dataset Columns

| Column               | Description                                   |
| -------------------- | --------------------------------------------- |
| `Name`               | Patient name                                  |
| `Age`                | Patient age                                   |
| `Gender`             | Patient gender                                |
| `Blood Type`         | Patient blood type                            |
| `Medical Condition`  | Medical condition associated with the patient |
| `Date of Admission`  | Patient admission date                        |
| `Doctor`             | Doctor associated with the patient            |
| `Hospital`           | Hospital associated with the patient          |
| `Insurance Provider` | Patient insurance provider                    |
| `Billing Amount`     | Healthcare billing amount                     |
| `Room Number`        | Patient room number                           |
| `Admission Type`     | Type of hospital admission                    |
| `Discharge Date`     | Patient discharge date                        |
| `Medication`         | Medication associated with the patient        |
| `Test Results`       | Medical test result                           |

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

The following Python libraries are used:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

* **Pandas** is used for data manipulation and analysis.
* **Matplotlib** is used for plotting.
* **Seaborn** is used for statistical visualizations.

---

### 2. Load the Dataset

The dataset is loaded using Pandas:

```python
df = pd.read_csv("/content/sample_data/healthcare_dataset (1).csv")
```

The first few records are displayed using `df.head()`.

---

## 🔍 Dataset Exploration

The notebook uses `df.info()` to inspect the dataset structure.

### Dataset Information

* **55,500 records**
* **15 columns**
* **1 float column**
* **2 integer columns**
* **12 object/string columns**

All 55,500 records contain values for the listed columns.

---

## 📊 Descriptive Statistics

The project uses `df.describe()` to analyze the numerical variables.

### Age

| Statistic          | Value |
| ------------------ | ----: |
| Mean               | 51.54 |
| Minimum            |    13 |
| Maximum            |    89 |
| Standard Deviation | 19.60 |

### Billing Amount

| Statistic          |     Value |
| ------------------ | --------: |
| Mean               | 25,539.32 |
| Minimum            | -2,008.49 |
| Maximum            | 52,764.28 |
| Standard Deviation | 14,211.45 |

### Room Number

| Statistic |  Value |
| --------- | -----: |
| Mean      | 301.13 |
| Minimum   |    101 |
| Maximum   |    500 |

---

## 🧹 Missing Value Analysis

The project checks for missing values using:

```python
df.isnull().sum()
```

The analysis shows **0 missing values across all 15 columns**.

---

## 📅 Admission Date Analysis

The `Date of Admission` column is converted into datetime format:

```python
df['Date of Admission'] = pd.to_datetime(df['Date of Admission'])
```

A `Year_Month` column is then created:

```python
df['Year_Month'] = df['Date of Admission'].dt.to_period('M')
```

This allows admissions to be grouped by month and year.

---

## 🏥 Monthly Admission Analysis

The project calculates the number of admissions for each month:

```python
monthly_admissions = df.groupby('Year_Month').size()
```

### Peak Admission Month

The highest number of admissions occurred in:

**August 2020**

with:

**1,014 admissions**

---

## 💰 Billing Analysis

The project compares total billing amounts based on:

* Medical Condition
* Insurance Provider

The data is grouped using:

```python
billing_data = df.groupby(
    ['Medical Condition', 'Insurance Provider']
)['Billing Amount'].sum().unstack(fill_value=0)
```

A **stacked bar chart** is then created to compare total billing amounts across medical conditions and insurance providers.

---

## 🎻 Billing Distribution by Medical Condition

A violin plot is used to visualize the distribution of billing amounts for different medical conditions.

The medical conditions analyzed are:

* Arthritis
* Asthma
* Cancer
* Diabetes
* Hypertension
* Obesity

This visualization helps compare the spread and distribution of billing amounts across the different medical conditions.

---

## 🏦 Billing Distribution by Insurance Provider

A second violin plot is created to analyze billing amount distributions across insurance providers.

The providers included are:

* Aetna
* Blue Cross
* Cigna
* Medicare
* UnitedHealthcare

---

## 📊 Average Billing Amount by Medical Condition

The notebook calculates the average billing amount for each medical condition.

| Medical Condition | Average Billing Amount |
| ----------------- | ---------------------: |
| Arthritis         |              25,497.33 |
| Asthma            |              25,635.25 |
| Cancer            |              25,161.79 |
| Diabetes          |              25,638.41 |
| Hypertension      |              25,497.10 |
| Obesity           |              25,805.97 |

---

## 🏦 Average Billing Amount by Insurance Provider

The project also calculates the average billing amount for each insurance provider.

| Insurance Provider | Average Billing Amount |
| ------------------ | ---------------------: |
| Aetna              |              25,553.29 |
| Blue Cross         |              25,613.01 |
| Cigna              |              25,525.77 |
| Medicare           |              25,615.99 |
| UnitedHealthcare   |              25,389.17 |

---

## 📈 Monthly Admission Pattern

The project extracts the admission month from the admission date:

```python
df['Admission Month'] = df['Date of Admission'].dt.month
```

The number of admissions for each calendar month is then calculated.

| Month | Admissions |
| ----: | ---------: |
|     1 |      4,692 |
|     2 |      4,255 |
|     3 |      4,672 |
|     4 |      4,518 |
|     5 |      4,599 |
|     6 |      4,699 |
|     7 |      4,812 |
|     8 |      4,832 |
|     9 |      4,546 |
|    10 |      4,678 |
|    11 |      4,548 |
|    12 |      4,649 |

A line chart is used to visualize this monthly admission pattern.

---

## 🔗 Correlation Analysis

The project calculates the correlation between:

* `Age`
* `Billing Amount`

```python
correlation_matrix = df[["Age", "Billing Amount"]].corr()
```

### Correlation Result

|                |       Age | Billing Amount |
| -------------- | --------: | -------------: |
| Age            |  1.000000 |      -0.003832 |
| Billing Amount | -0.003832 |       1.000000 |

The calculated correlation between **Age and Billing Amount is -0.003832**.

A heatmap is used to visualize this correlation matrix.

---

## 📊 Visualizations

The project contains the following visualizations:

1. **Stacked Bar Chart**

   * Total billing amount by medical condition and insurance provider.

2. **Violin Plot – Medical Condition**

   * Billing amount distribution across medical conditions.

3. **Violin Plot – Insurance Provider**

   * Billing amount distribution across insurance providers.

4. **Line Chart**

   * Monthly admission trend.

5. **Correlation Heatmap**

   * Relationship between age and billing amount.

---

## 🔍 Key Findings

Based on the analysis performed in the notebook:

* The dataset contains **55,500 healthcare records**.
* There are **15 columns** in the dataset.
* No missing values were found in the analyzed columns.
* The average patient age is approximately **51.54 years**.
* The average billing amount is approximately **25,539.32**.
* The highest number of admissions for a specific year-month occurred in **August 2020**, with **1,014 admissions**.
* Across calendar months, **August has the highest number of admissions with 4,832 records**.
* Average billing amounts are relatively close across the different medical conditions and insurance providers.
* The correlation between age and billing amount is **-0.003832**.

---

## 📁 Project Structure

```text
Healthcare-Data-Analysis/
│
├── healthcare.ipynb
├── healthcare_dataset (1).csv
└── README.md
```

---

## ▶️ How to Run the Project

### Using Google Colab

1. Open `healthcare.ipynb` in Google Colab.
2. Upload `healthcare_dataset (1).csv`.
3. Make sure the CSV file path matches the path used in the notebook.
4. Run the notebook cells sequentially.

### Using Jupyter Notebook

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

Then open the notebook:

```bash
jupyter notebook healthcare.ipynb
```

Place the healthcare CSV dataset in the required directory and run the notebook cells.

---

## 📌 Conclusion

This project provides an exploratory analysis of healthcare data using Python.

The analysis covers dataset exploration, missing-value checking, descriptive statistics, admission trends, billing analysis, medical-condition comparisons, insurance-provider comparisons, monthly admission patterns, and correlation analysis.

The visualizations make it easier to compare billing amounts, observe admission patterns, and understand the relationship between selected numerical variables.

---

## 👨‍💻 Project Type

**Healthcare Data Analysis / Exploratory Data Analysis (EDA)**

**Tools:** Python, Pandas, Matplotlib, Seaborn

**Dataset:** Healthcare Patient Records
