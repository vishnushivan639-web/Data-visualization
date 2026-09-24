📊 Superstore Sales Data Analysis

Project Overview

This project performs Exploratory Data Analysis (EDA) on a
Superstore sales dataset using Python.

The notebook focuses on loading the dataset, exploring its structure,
handling date fields, creating a delivery-time feature, checking data
quality, analyzing sales by category, and visualizing the results.

🎯 Objectives

Explore the Superstore sales dataset.

Understand the dataset structure and data types.

Convert order and shipping dates into datetime format.

Calculate delivery duration.

Identify available product categories.

Check for missing values.

Analyze total sales by category.

Visualize category-wise sales.

Understand the sales data through basic analysis and visualization.

🗂️ Dataset

The project uses the Superstore dataset loaded from an Excel file.

Dataset Details

Rows: 10,194

Original columns: 21

Columns after feature creation: 22

Main Features

Row ID

Order ID

Order Date

Ship Date

Ship Mode

Customer ID

Customer Name

Segment

Country/Region

City

State/Province

Postal Code

Region

Product ID

Category

Sub-Category

Product Name

Sales

Quantity

Discount

Profit

Delivery Days

🛠️ Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Google Colab / Jupyter Notebook

Excel

🔍 Analysis Workflow

1. Import Libraries

The notebook uses Pandas and NumPy for data processing and Matplotlib
and Seaborn for visualization.

import pandas as pd
import numpy as np

import matplotlib.pyplot as plt
import seaborn as sns

2. Load the Dataset

The Excel dataset is loaded into a Pandas DataFrame.

df = pd.read_excel("/content/sample_data/samplesuperstore.xlsx")

3. Explore the Dataset

The notebook uses:

df.head() to view the first records.

df.info() to understand columns, data types, and non-null values.

The dataset contains 10,194 records and 21 columns before adding the
new feature.

4. Date Processing

The Order Date and Ship Date columns are converted to datetime
format.

df['Order Date'] = pd.to_datetime(df['Order Date'])
df['Ship Date'] = pd.to_datetime(df['Ship Date'])

5. Feature Creation

A new Delivery Days column is created by calculating the difference
between shipping date and order date.

df['Delivery Days'] = (
    df['Ship Date'] - df['Order Date']
).dt.days

After this step, the dataset contains 22 columns.

6. Category Analysis

The notebook identifies three product categories:

Office Supplies

Furniture

Technology

df['Category'].unique()

7. Missing Value Check

Missing values are checked using:

df.isnull().sum()

The notebook output shows 0 missing values across all 22 columns.

📈 Sales Analysis by Category

The total sales for each category are calculated using groupby().

category_sales = df.groupby('Category')['Sales'].sum()

Results

Category             Total Sales

Furniture           754,747.7613
Office Supplies     731,893.3140
Technology          839,893.2790

The notebook also creates a bar chart titled "Sales by Category" to
visualize the total sales for each category.

💡 Key Findings

The dataset contains 10,194 records.

The analysis works with 21 original columns and creates
Delivery Days as an additional feature.

The dataset contains three categories: Office Supplies, Furniture,
and Technology.

The notebook reports no missing values in the analyzed columns.

Category-wise sales were calculated using Pandas groupby().

A bar chart was used to visualize sales by category.

The calculated category sales values are highest for Technology
among the three categories.

📁 Project Structure

Superstore-Sales-Data-Analysis/
│
├── sample superstore.ipynb
├── samplesuperstore.xlsx
└── README.md

▶️ How to Run

Open the notebook in Google Colab or Jupyter Notebook.

Upload the samplesuperstore.xlsx dataset.

Update the dataset path if required.

Run the notebook cells in order.

View the generated tables and sales visualization.

🚀 Skills Demonstrated

Python programming

Pandas DataFrame operations

NumPy basics

Data exploration

Data type handling

Date/time processing

Feature creation

Missing value analysis

GroupBy aggregation

Sales analysis

Data visualization

Matplotlib and Seaborn

📌 Project Type

Python Data Analysis / Exploratory Data Analysis (EDA)

📚 Learning Outcome

Through this project, I practiced working with a real-world style sales
dataset and learned how to explore data, process date columns, create
new features, check data quality, perform category-wise analysis, and
communicate results through visualization.
