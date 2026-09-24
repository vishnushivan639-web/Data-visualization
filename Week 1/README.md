Superstore Sales Data Analysis

📊 Project Overview

This project analyzes a Superstore sales dataset using Python to
understand sales performance, product categories, delivery time, and
sales distribution.

The analysis was performed using Pandas, NumPy, Matplotlib, and
Seaborn in a Jupyter/Google Colab notebook.

🎯 Objectives

Explore and understand the sales dataset.

Check the structure and data types of the dataset.

Convert order and shipping dates into datetime format.

Calculate delivery time in days.

Check available product categories.

Check for missing values.

Analyze total sales by category.

Visualize sales by category.

Understand the distribution of sales values.

🗂️ Dataset

The project uses a Superstore dataset loaded from an Excel file.

Dataset size: - 10,194 records - 21 original columns - 22 columns
after adding Delivery Days

Main Columns

Order ID

Order Date

Ship Date

Ship Mode

Customer ID

Customer Name

Segment

Region

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

Pandas -- data loading, cleaning, grouping, and analysis

NumPy -- numerical operations

Matplotlib -- data visualization

Seaborn -- statistical visualization

Jupyter Notebook / Google Colab

Excel -- source dataset

🔍 Data Analysis Process

1. Data Loading

The Excel dataset was loaded into a Pandas DataFrame.

2. Data Exploration

Used: - head() to view sample records - info() to understand columns
and data types - describe() to view numerical statistics

3. Date Processing

Order Date and Ship Date were converted to datetime format.

A new column, Delivery Days, was calculated:

df['Delivery Days'] = (df['Ship Date'] - df['Order Date']).dt.days

4. Data Quality Check

Missing values were checked using:

df.isnull().sum()

The notebook shows 0 missing values across the analyzed columns.

5. Category Analysis

The dataset contains three main categories:

Office Supplies

Furniture

Technology

Total sales were grouped by category.

📈 Sales by Category

Category             Total Sales

Technology          839,893.2790
Furniture           754,747.7613
Office Supplies     731,893.3140

The notebook also visualizes these values using a bar chart titled
"Sales by Category".

📊 Sales Distribution

A histogram with 30 bins was created using Seaborn to understand how
individual sales values are distributed across the dataset.

💡 Key Findings

The dataset contains 10,194 records.

There are three product categories: Technology, Furniture, and
Office Supplies.

The category-level sales analysis shows different sales
contributions across the three categories.

Delivery Days was derived from the difference between shipping and
order dates.

The data quality check reported no missing values in the
analyzed columns.

Visualizations were used to make category-level sales and sales
distribution easier to understand.

📁 Project Structure

Superstore-Sales-Data-Analysis/
│
├── Superstore_Sales_Analysis.ipynb
├── samplesuperstore.xlsx
└── README.md

▶️ How to Run

Download or clone the project.

Open Superstore_Sales_Analysis.ipynb in Jupyter Notebook or Google
Colab.

Place samplesuperstore.xlsx in the expected dataset location.

Run the notebook cells from top to bottom.

View the generated tables and visualizations.

🚀 Skills Demonstrated

Data loading and exploration

Data cleaning and validation

Date/time handling

Feature creation

GroupBy analysis

Statistical summary

Data visualization

Python-based exploratory data analysis

👩‍💻 Project Type

Python Data Analysis / Exploratory Data Analysis (EDA) Project

📌 Note

This README is based on the analysis implemented in the provided
notebook. It describes the operations and results present in the
notebook without adding unsupported analysis.
