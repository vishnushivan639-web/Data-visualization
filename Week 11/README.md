

# Week 11 – Automobile Dataset Data Cleaning and Feature Engineering

## Project Overview

This project focuses on cleaning, transforming, and analyzing the Automobile Dataset using Python. The main objective is to prepare the dataset for further visualization and data analysis by handling missing values, converting data types, creating new features, and performing statistical analysis.

## Dataset

- **Dataset Name:** Automobile Dataset
- **Source:** [Kaggle – Automobile Dataset](https://www.kaggle.com/datasets/toramky/automobile-dataset)
- **Library Used:** Pandas, NumPy, Matplotlib, Seaborn

## Tasks Performed

### Task 1: Import Libraries and Load the Dataset
- Imported Pandas and NumPy for data manipulation.
- Imported Matplotlib and Seaborn for data visualization.
- Loaded the Automobile Dataset into a Pandas DataFrame.
- Displayed the first five and last five records.
- Identified the number of rows, columns, and column names.

### Task 2: Understand Dataset Structure
- Examined the dataset using `df.info()`.
- Generated statistical summaries using `df.describe()`.
- Identified categorical and numerical attributes.
- Examined data types and non-null counts.

### Task 3: Detect and Replace Non-Standard Missing Values
- Identified `?` markers representing missing values.
- Replaced non-standard missing values with NumPy NaN.
- Calculated missing values in each column.
- Identified columns with a high percentage of missing values.

### Task 4: Handle Missing Values Using Category Medians
- Identified missing values in horsepower, peak-rpm, bore, stroke, and price.
- Applied category-wise median imputation using make, body-style, and fuel-type.
- Used the overall column median as a fallback.
- Verified the missing values after imputation.

### Task 5: Convert Columns into Numerical Data Types
- Converted horsepower into integer format.
- Converted peak-rpm, price, bore, and stroke into floating-point format.
- Converted other technical numerical columns into suitable numerical types.
- Verified the updated data types.

### Task 6: Feature Engineering – Power-to-Weight Ratio
- Identified horsepower and curb-weight columns.
- Created a new feature named `power_to_weight_ratio`.
- Calculated the ratio using horsepower and curb weight.
- Compared the values across automobile models.

### Task 7: Feature Engineering – Combined Fuel Consumption
- Identified city-mpg and highway-mpg columns.
- Created a new feature named `combined_mpg`.
- Calculated the average fuel efficiency using city and highway MPG.
- Compared fuel efficiency across automobile models.

### Task 8: Statistical Summary Across Body Styles
- Grouped vehicles based on body-style.
- Calculated average horsepower.
- Calculated average engine size.
- Calculated average curb weight.
- Calculated average price.
- Calculated average combined MPG.

### Task 9: Statistical Summary Across Engine Locations
- Grouped vehicles based on engine-location.
- Calculated average horsepower.
- Calculated average engine size.
- Calculated average curb weight.
- Calculated average price.
- Compared front-engine and rear-engine vehicles.

### Task 10: Final Data Validation and Export
- Checked for remaining missing values.
- Verified numerical data types.
- Checked duplicate records.
- Validated newly created features.
- Reviewed the final dataset structure.
- Exported the cleaned dataset as `automobile_cleaned.csv`.

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

## New Features Created

| Feature | Description |
|---|---|
| `power_to_weight_ratio` | Measures engine horsepower relative to vehicle weight |
| `combined_mpg` | Represents the average of city MPG and highway MPG |

## Project Output

The final cleaned and transformed dataset is exported as:

`automobile_cleaned.csv`

This dataset contains cleaned numerical specifications and newly engineered features. It is prepared for further visualization and analysis in Week 12.

## Learning Outcomes

- Learned to load and examine datasets using Pandas.
- Understood how to identify and handle non-standard missing values.
- Practiced category-wise median imputation.
- Learned numerical data type conversion.
- Applied feature engineering techniques.
- Performed group-wise statistical analysis.
- Validated and exported a cleaned dataset.

