# House Sales Data Cleaning and Valuation Analysis

## 📌 Project Overview

This project focuses on cleaning and transforming house sales data to analyze property features, calculate property age and renovation details, derive price-per-square-foot metrics, and identify valuation outliers using statistical methods and box plots.

The project uses Python data analysis libraries to prepare and examine the King County house sales dataset.

## 🎯 Objectives

- Inspect property features such as bedrooms, bathrooms, living area, grade, and year built.
- Extract temporal attributes from sale dates.
- Calculate property age and renovation-related features.
- Compute price per square foot for living area and total lot size.
- Identify extreme property valuation outliers using statistical bounds and box plots.

## 🛠️ Technologies Used

- **Python**
- **Pandas** – Data handling and transformation
- **NumPy** – Numerical calculations and derived features
- **Matplotlib** – Data visualization
- **Seaborn** – Box plot visualization
- **Google Colab / Jupyter Notebook** – Development environment

## 📂 Dataset

The project uses the `kc_house_data.csv` dataset containing house sales information.

Important columns include:

- `price` – House sale price
- `bedrooms` – Number of bedrooms
- `bathrooms` – Number of bathrooms
- `sqft_living` – Living area in square feet
- `sqft_lot` – Total lot size in square feet
- `grade` – Property construction and design grade
- `yr_built` – Year the property was built
- `yr_renovated` – Year of renovation, if recorded
- `date` – House sale date

## ⚙️ Project Workflow

### 1. Data Loading and Exploration

- Loaded the dataset using Pandas.
- Inspected the first and last records.
- Examined dataset structure, column names, dimensions, and descriptive statistics.
- Checked for missing values and duplicate records.

### 2. Date Processing and Feature Engineering

- Converted sale dates into datetime format.
- Extracted the sale year.
- Calculated property age.
- Created an `is_renovated` indicator.
- Calculated years since renovation for renovated properties.

### 3. Price per Square Foot

Created two valuation metrics:

- `price_per_sqft_living` = House price / Living area
- `price_per_sqft_lot` = House price / Total lot size

Zero denominators are replaced with missing values to avoid division-by-zero errors.

### 4. Statistical Outlier Detection

Used the Interquartile Range (IQR) method to identify potential outliers.

- Q1: 25th percentile
- Q3: 75th percentile
- IQR: Q3 − Q1
- Lower bound: Q1 − 1.5 × IQR
- Upper bound: Q3 + 1.5 × IQR

Values outside these bounds are flagged as potential outliers for further examination.

### 5. Data Visualization

Generated separate box plots for:

- Price per square foot of living area
- Price per square foot of total lot size

These plots help visualize the distribution of valuation metrics and potential extreme values.

## 📊 Expected Outcomes

- Better understanding of house sales data.
- Creation of useful property age and renovation features.
- Calculation of living-area and lot-size valuation metrics.
- Identification of potential valuation outliers.
- Visual understanding of valuation distributions through box plots.

## ▶️ How to Run the Project

1. Download or clone this repository.
2. Open `kc_house.ipynb` in Google Colab or Jupyter Notebook.
3. Upload `kc_house_data.csv` to the expected location.
4. Install the required libraries if they are not already available.
5. Run the notebook cells in order.

## 🚀 Future Improvements

- Handle missing values systematically across all relevant columns.
- Compare valuation metrics across property grades and age groups.
- Investigate potential outliers before deciding whether to remove them.
- Create additional visualizations to explore price trends.

## 👩‍💻 Author

**Vishnu Lakshmi A**

BCA Student | Python | Data Analysis 

