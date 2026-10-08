# Student Performance Data Analysis

## 📌 Project Overview

This project focuses on analyzing student performance using Python and data visualization techniques. The analysis explores students' Math, Reading, and Writing scores along with demographic and educational factors.

The project uses statistical analysis and visualizations to understand patterns, comparisons, relationships, and correlations in student performance.

---

## 🎯 Objectives

- Explore and understand the student performance dataset.
- Inspect the structure, columns, shape, and statistical summary of the data.
- Check for missing values.
- Analyze numerical score columns.
- Analyze demographic and categorical features.
- Compare average subject scores based on parental education.
- Compare average scores based on parental education and lunch type.
- Analyze score variance based on test preparation course.
- Study the relationship between Math and Reading scores.
- Analyze correlations among Math, Reading, and Writing scores.

---

## 📊 Dataset Information

The dataset contains **1,000 student records and 10 columns**.

### Features

| Column | Description |
|---|---|
| gender | Gender of the student |
| race/ethnicity | Race/Ethnicity group |
| parental level of education | Parent's highest education level |
| lunch | Lunch type |
| test preparation course | Test preparation course status |
| math score | Math score |
| reading score | Reading score |
| writing score | Writing score |
| Total Score | Total score |
| Percentage | Overall percentage |

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab

---

## 🔍 Data Exploration

The following techniques were used to understand the dataset:

- `df.head()` – Displays the first records.
- `df.tail()` – Displays the last records.
- `df.info()` – Checks data types and dataset structure.
- `df.columns` – Displays column names.
- `df.shape` – Displays the number of rows and columns.
- `df.describe()` – Provides statistical summary.
- `df.isnull().sum()` – Checks for missing values.

### Missing Values

The dataset contains **0 missing values** across all columns.

---

## 📈 Statistical Analysis

The main subject statistics were analyzed using:

- Mean
- Median
- Standard Deviation
- First Quartile (Q1)
- Third Quartile (Q3)

### Subject Statistics

| Subject | Mean | Median | Standard Deviation | Q1 | Q3 |
|---|---:|---:|---:|---:|---:|
| Math | 66.089 | 66 | 15.163 | 57 | 77 |
| Reading | 69.169 | 70 | 14.600 | 59 | 79 |
| Writing | 68.054 | 69 | 15.196 | 57.75 | 79 |

### Overall Results

- Average Total Score: **203.312**
- Average Percentage: **67.771%**
- Maximum Total Score: **300**
- Maximum Percentage: **100%**

---

## 📊 Data Visualization

### 1. Grouped Bar Chart – Parental Education

A grouped bar chart is used to compare the average:

- Math Score
- Reading Score
- Writing Score

based on the **parental level of education**.

This helps understand how average student performance varies across different parental education levels.

---

### 2. Grouped Bar Chart – Parental Education and Lunch Type

The average score of students is compared based on:

- Parental level of education
- Lunch type

This visualization helps identify differences in average performance between different groups.

---

### 3. Box Plot – Test Preparation Course

A box plot is used to compare the distribution of students' average scores based on their test preparation course status.

The two groups are:

- Completed
- None

The box plot helps understand score distribution and variation between the groups.

---

### 4. Scatter Plot – Math vs Reading

A scatter plot is created to analyze the relationship between:

- Math Score
- Reading Score

**X-axis:** Math Score  
**Y-axis:** Reading Score

This helps visualize whether students who perform well in Math also tend to perform well in Reading.

---

### 5. Correlation Heatmap

A correlation matrix is created for:

- Math Score
- Reading Score
- Writing Score

A heatmap is used to visualize the strength of relationships between the subjects.

---

## 🧮 Calculated Features

The project calculates students' average scores using:

```python
df["Average"] = df[["math score", "reading score", "writing score"]].mean(axis=1)
