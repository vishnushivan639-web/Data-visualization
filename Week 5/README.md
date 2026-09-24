# Healthcare Data Analysis

## 📌 Project Overview

This project performs a basic analysis of **healthcare patient data** using Python.

The analysis focuses on medical codes, standardizing medical codes, admission and discharge dates, hospital stay duration, and billing amount statistics.

The project uses **Pandas, Matplotlib, and Seaborn** for data analysis.

---

## 🎯 Objectives

The main objectives of this project are:

* Load and explore healthcare dataset information.
* Analyze the distribution of medical codes.
* Check the availability of medical-code values.
* Standardize medical codes by removing the `ICD-10-` prefix.
* Convert admission and discharge dates into datetime format.
* Calculate the number of days each patient stayed in the hospital.
* Analyze billing amount statistics.
* Analyze hospital stay duration statistics.

---

## 📂 Dataset

The project uses a CSV dataset named:

`healthcare_dataset.csv`

The dataset contains healthcare-related patient records, including medical codes, admission dates, discharge dates, and billing amounts.

### Dataset Information

The analysis contains **500 records** for the variables used in the statistical analysis.

### Main Features Used

| Column                      | Description                                          |
| --------------------------- | ---------------------------------------------------- |
| `Medical_Code`              | Medical/diagnostic code associated with the record   |
| `Admission_Date`            | Date on which the patient was admitted               |
| `Discharge_Date`            | Date on which the patient was discharged             |
| `Billing_Amount`            | Billing amount associated with the healthcare record |
| `Standardized_Medical_Code` | Medical code after removing the `ICD-10-` prefix     |
| `Hospital_Stay_Days`        | Number of days between admission and discharge       |

---

## 🛠️ Technologies Used

* Python
* Pandas
* Matplotlib
* Seaborn
* Jupyter Notebook / Google Colab

---

## 🔄 Project Workflow

### 1. Import Libraries

The project imports the following libraries:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

* **Pandas** is used for data loading and manipulation.
* **Matplotlib** and **Seaborn** are imported for data visualization.

---

### 2. Load the Dataset

The healthcare dataset is loaded using Pandas:

```python
df = pd.read_csv("/content/sample_data/healthcare_dataset.csv")
```

The dataset is then displayed for exploration.

---

## 🏥 Medical Code Analysis

The project checks the medical-code column:

```python
df['Medical_Code'].isnull()
```

The distribution of medical codes is then calculated using:

```python
df['Medical_Code'].value_counts()
```

### Medical Code Frequency

Some of the medical codes and their frequencies are:

| Medical Code | Count |
| ------------ | ----: |
| ICD-10-J44   |    34 |
| ICD-10-K35   |    33 |
| ICD-10-I63   |    33 |
| ICD-10-J18   |    31 |
| ICD-10-I50   |    30 |
| ICD-10-N20   |    28 |
| ICD-10-I10   |    28 |
| ICD-10-I21   |    27 |
| ICD-10-S52   |    22 |
| ICD-10-K29   |    21 |

The notebook identifies **25 distinct medical codes** in the displayed frequency results.

---

## 🔤 Medical Code Standardization

The project creates a new column called:

`Standardized_Medical_Code`

The `ICD-10-` prefix is removed from the original medical code:

```python
df['Standardized_Medical_Code'] = df['Medical_Code'].str.replace('ICD-10-', '')
```

### Example

| Medical Code | Standardized Code |
| ------------ | ----------------- |
| ICD-10-I10   | I10               |
| ICD-10-J18   | J18               |
| ICD-10-E11   | E11               |
| ICD-10-J45   | J45               |
| ICD-10-S52   | S52               |

This makes the medical codes simpler and easier to work with.

---

## 📅 Date Processing

The project converts both admission and discharge dates into Pandas datetime format:

```python
df['Admission_Date'] = pd.to_datetime(
    df['Admission_Date'],
    format='%d-%m-%Y'
)

df['Discharge_Date'] = pd.to_datetime(
    df['Discharge_Date'],
    format='%d-%m-%Y'
)
```

This allows the project to perform date-based calculations.

---

## 🏨 Hospital Stay Calculation

A new feature called `Hospital_Stay_Days` is created.

```python
df['Hospital_Stay_Days'] = (
    df['Discharge_Date'] -
    df['Admission_Date']
).dt.days
```

This calculates the number of days between the admission date and discharge date.

### Hospital Stay Statistics

| Statistic          |    Days |
| ------------------ | ------: |
| Count              |     500 |
| Mean               |   2.744 |
| Standard Deviation | 1.17696 |
| Minimum            |       1 |
| 25th Percentile    |       2 |
| Median             |       2 |
| 75th Percentile    |       4 |
| Maximum            |      10 |

The average hospital stay in the analyzed records is approximately **2.74 days**.

---

## 💰 Billing Amount Analysis

The project uses descriptive statistics to analyze the `Billing_Amount` column.

### Billing Statistics

| Statistic          |      Amount |
| ------------------ | ----------: |
| Count              |         500 |
| Mean               |   7,249.001 |
| Standard Deviation | 3,198.96932 |
| Minimum            |       2,300 |
| 25th Percentile    |       4,400 |
| Median             |       6,950 |
| 75th Percentile    |       9,400 |
| Maximum            |      14,200 |

The average billing amount in the analyzed records is **7,249.001**.

---

## 🔍 Key Findings

Based on the analysis performed in the notebook:

* The dataset contains **500 records** for the analyzed billing and hospital-stay variables.
* **25 medical codes** are shown in the medical-code frequency analysis.
* `Medical_Code` values are standardized by removing the `ICD-10-` prefix.
* Admission and discharge dates are converted to datetime format.
* Hospital stay duration is calculated from admission and discharge dates.
* The average hospital stay is approximately **2.74 days**.
* Hospital stays range from **1 to 10 days**.
* The average billing amount is approximately **7,249.001**.
* Billing amounts range from **2,300 to 14,200**.

---

## 📁 Project Structure

```text
Healthcare-Data-Analysis/
│
├── health care.ipynb
├── healthcare_dataset.csv
└── README.md
```

---

## ▶️ How to Run the Project

### Using Google Colab

1. Open `health care.ipynb` in Google Colab.
2. Upload `healthcare_dataset.csv`.
3. Make sure the dataset path matches the path used in the notebook.
4. Run the notebook cells sequentially.

### Using Jupyter Notebook

Install the required libraries:

```bash
pip install pandas matplotlib seaborn
```

Then open the notebook:

```bash
jupyter notebook "health care.ipynb"
```

Place `healthcare_dataset.csv` in the appropriate directory and run the notebook cells.

---

## 📌 Conclusion

This project demonstrates a basic **Healthcare Data Analysis** workflow using Python.

The analysis includes medical-code frequency analysis, medical-code standardization, date conversion, hospital stay calculation, and descriptive statistical analysis of billing amounts and hospital stay durations.

The project demonstrates how healthcare-related data can be cleaned, transformed, and summarized using Pandas.
