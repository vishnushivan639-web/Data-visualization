Student Performance Data Analysis
📌 Project Overview
This project analyzes a Student Performance dataset using Python, Pandas, NumPy, Matplotlib, and Seaborn. The analysis focuses on students' Math, Reading, and Writing scores and explores how demographic and educational factors are related to academic performance.
The project also creates visualizations to understand score patterns, group comparisons, score variance, relationships between subjects, and correlations.
🎯 Objectives
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
📊 Dataset Information
The dataset contains 1,000 student records and 10 columns.
Columns
Column	Description
gender	Gender of the student
race/ethnicity	Race/ethnicity group
parental level of education	Parent's highest education level
lunch	Lunch type
test preparation course	Test preparation course status
math score	Math score
reading score	Reading score
writing score	Writing score
Total Score	Total score across the three subjects
Percentage	Overall percentage


Categorical Features
- Gender: female, male
- Race/Ethnicity: Groups A–E
- Parental Education:
  - bachelor's degree
  - some college
  - master's degree
  - associate's degree
  - high school
  - some high school
- Lunch:
  - standard
  - free/reduced
- Test Preparation:
  - completed
  - none
🛠️ Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab
🔍 Data Exploration
The notebook performs basic exploratory data analysis using:
- df.info() – checks dataset structure and data types.
- df.head() – displays the first records.
- df.tail() – displays the last records.
- df.columns – displays column names.
- df.describe() – generates statistical summaries.
- df.isnull().sum() – checks missing values.
- df.shape – checks the number of rows and columns.
Missing Values
The analysis shows 0 missing values across all 10 columns.
📈 Statistical Summary
The main subject statistics obtained from the dataset are:
Subject	Mean	Median	Std. Dev.	Q1	Q3
Math	66.089	66	15.163	57	77
Reading	69.169	70	14.600	59	79
Writing	68.054	69	15.196	57.75	79


Overall:
- Average Total Score: 203.312
- Average Percentage: 67.771%
- Maximum Total Score: 300
- Maximum Percentage: 100%
📊 Data Visualization
1. Grouped Bar Chart – Parental Education
The project groups students by parental level of education and calculates the average Math, Reading, and Writing scores.
This visualization helps compare academic performance across different parental education levels.
2. Grouped Bar Chart – Parental Education and Lunch Type
An Average score is calculated from Math, Reading, and Writing scores.
The analysis then compares average student scores using:
- Parental education
- Lunch type
This helps observe differences in average performance across these groups.
3. Box Plot – Test Preparation Course
An Average Score is calculated for every student.
A box plot is then used to compare score variance between students who:
- Completed the test preparation course
- Did not complete the test preparation course
The box plot helps visualize the distribution and variation of average scores.
4. Scatter Plot – Math vs Reading
A scatter plot is created using:
- X-axis → Math Score
- Y-axis → Reading Score
This visualization helps examine the relationship between Math and Reading performance.
5. Correlation Heatmap
A correlation matrix is calculated for:
- Math Score
- Reading Score
- Writing Score
The heatmap displays correlation values between the three subjects, making it easier to identify how strongly the subjects are related.
🧮 Calculated Features
The notebook uses calculated average scores for visualization:
Average
df["Average"] = df[["math score", "reading score", "writing score"]].mean(axis=1)
Average Score
df["Average Score"] = df[["math score", "reading score",
                          "writing score"]].mean(axis=1)
The dataset already contains:
- Total Score
- Percentage
These are used as part of the dataset analysis.
💡 Key Learning Outcomes
Through this project, I practiced:
- Loading datasets using Pandas
- Understanding DataFrame structure
- Inspecting columns and data types
- Checking missing values
- Performing descriptive statistics
- Working with categorical and numerical data
- Grouping data using groupby()
- Calculating average scores
- Creating Bar Charts
- Creating Box Plots
- Creating Scatter Plots
- Creating Correlation Heatmaps
- Understanding relationships between variables
- Using Matplotlib for visualization
- Using Pandas plotting functions for data analysis
📁 Project Structure
Student-Performance-Data-Analysis/
│
├── Week_8.ipynb
├── studentperformance_preprocessed.csv
└── README.md
▶️ How to Run
1. Open Week_8.ipynb in Jupyter Notebook or Google Colab.
2. Make sure the dataset is available at the required path.
3. Install the required libraries if needed:
pip install pandas numpy matplotlib seaborn
4. Run the notebook cells in order.
5. View the generated statistics and visualizations.
🚀 Conclusion
This project provides an exploratory analysis of student performance across Math, Reading, and Writing. By combining statistical analysis with visualizations such as bar charts, box plots, scatter plots, and correlation heatmaps, the project demonstrates how Python can be used to understand patterns and relationships in educational data.
👩‍💻 Skills Demonstrated
Python | Pandas | NumPy | Matplotlib | Seaborn | Data Analysis | Exploratory Data Analysis | Data Visualization
