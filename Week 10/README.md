# Week 10: House Price Visualization, Spatial Analytics & Real-Estate Insights

## Project Overview

This project focuses on analyzing house prices using the King County House Sales Dataset. It explores the relationships between property characteristics, geographical location, and sale prices through data visualization and statistical analysis.

The preprocessed dataset from Week 9 is used to identify pricing patterns, compare property valuations, and investigate geographical clusters of high-value properties.

## Dataset

- **Dataset Name:** King County House Sales Dataset
- **Source:** [Kaggle – House Sales in King County, USA](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction)
- **Input Dataset:** `kc_house_data.csv` (Preprocessed Week 9 dataset)

The dataset includes house prices, living area, lot size, bedrooms, bathrooms, grade, condition, waterfront access, latitude, longitude, property age, renovation status, and price-per-square-foot metrics.

## Objectives

- Analyze the relationship between living area and house prices.
- Compare house price distributions across property grades and conditions.
- Examine price differences between waterfront and non-waterfront properties.
- Visualize geographical house price patterns using latitude and longitude.
- Analyze property age, renovation status, bedrooms, bathrooms, and price per square foot.
- Identify geographical areas containing high-value properties.
- Generate evidence-based insights for real-estate market evaluation.

## Visualizations and Analysis

1. **Living Area and House Price Analysis**
   - Scatter plot with linear regression trend line.
   - Nonlinear trend line to examine pricing patterns.
   - Price-per-square-foot analysis to identify unusual valuations.

2. **Property Grade and Condition Analysis**
   - Box plot of house prices by grade.
   - Box plot of house prices by condition.
   - Comparison of median prices across categories.

3. **Waterfront Price Premium Analysis**
   - Box plot comparing waterfront and non-waterfront properties.
   - Calculation of observed median price differences.

4. **Geographic House Price Analysis**
   - Geographic scatter plot using latitude and longitude.
   - Price-based color visualization.
   - Comparison of geographical location and waterfront access.

5. **Multivariable Property Valuation Analysis**
   - Property age versus house price.
   - Renovated versus non-renovated property price comparison.
   - Average price per square foot by property grade.
   - Living area versus price per square foot.
   - House price comparison by bedroom and bathroom categories.

6. **Geographic Cluster Identification**
   - Identification of properties in the top 10% of sale prices.
   - Visualization of high-value property locations.
   - Summary of potential high-value areas using rounded geographical coordinates.

7. **Correlation Analysis**
   - Correlation heatmap for selected numerical variables.
   - Examination of relationships between house prices and property characteristics.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## How to Run the Project

1. Clone or download the project repository.
2. Place the preprocessed `kc_house_data.csv` file in the same folder as the notebook.
3. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

4. Open `Week_10.ipynb` using Jupyter Notebook or Google Colab.
5. Run the notebook cells in order to generate the visualizations and analysis results.

**Note:** Update the CSV filename or column names in the code if your dataset uses different names.

## Key Metrics

- Average and median house prices by grade and condition.
- Observed median price difference between waterfront and non-waterfront properties.
- Average house prices by renovation status.
- Average price per square foot across property grades.
- Correlation between house prices and selected property characteristics.
- Price threshold and geographical distribution of high-value properties.

## Results and Insights

The notebook generates charts and statistical summaries to investigate:

- How living area is associated with house prices.
- Which property grades and condition categories have higher median prices.
- Whether waterfront properties show a higher observed median price.
- How property age and renovation status relate to house prices.
- Where high-value property sales appear geographically concentrated.
- Which property characteristics may be relevant for further real-estate investment analysis.

Actual findings should be added after running the notebook and reviewing the generated outputs.

## Limitations

- The analysis identifies associations and does not establish causal relationships.
- House prices may be influenced by multiple factors, including location, property size, grade, condition, and waterfront access.
- Extreme values may affect averages, regression trends, and visualization scales.
- Geographic groups based on rounded coordinates are exploratory and do not represent formal clustering results.
- Findings depend on the quality and completeness of the preprocessed dataset.
- Observed price differences do not prove that a particular property characteristic caused the difference.

## Conclusion

This project uses data visualization, statistical summaries, and geographical analysis to investigate house price variation in King County. It compares property characteristics and spatial pricing patterns to identify relationships and potential areas for further investigation. The results can support exploratory real-estate market evaluation, while investment decisions require additional analysis of location, property characteristics, and market conditions.

## Project Files

- `Week_10.ipynb` – Python notebook containing visualizations and analysis.
- `kc_house_data.csv` – Preprocessed dataset required to run the notebook.
- `README.md` – Project documentation.
