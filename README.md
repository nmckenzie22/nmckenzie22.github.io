# Education and Income
## By Nick M, Jackson T, Harrison P
This contains a summary of the Final Project for DS 201. For more in-depth in-sight, please check out our walkthrough video or run our notebook directly in Google Colab linked below.
## Introduction

As data science students, we often look to data as a tool to illuminate persistent inequalities and uncover meaningful patterns that shape our society. In the United States, the connection between education and economic prosperity is frequently assumed to be direct and causal. Higher levels of education are believed to lead to higher incomes, better employment opportunities, and improved quality of life. But is this relationship as straightforward as it seems?

The U.S. education system is vast and varied, with counties across the country showing significant differences in degree attainment. According to the U.S. Census Bureau, educational attainment is one of the strongest predictors of economic mobility, but disparities in access to quality education remain a pressing issue. Rural counties, in particular, often face systemic barriers to both higher education and high-paying jobs. Understanding how education levels correlate with income at the county level is essential to evaluating the effectiveness of education policy and identifying communities that may be underserved.

At the same time, it is important to recognize that income is shaped by more than just education. Local industries, cost of living, historical inequality, and regional infrastructure also play key roles. While one county may see high earnings with modest degree attainment due to a dominant industry, another may struggle economically despite high educational levels. This complexity raises an important question: How strongly does educational attainment, specifically the percentage of residents with associate or bachelor’s degrees,predict per capita income across U.S. counties?

To explore this, we analyzed a dataset that includes income data from 2019 to 2021 and education statistics spanning from 2015 to 2020. By comparing these variables across hundreds of U.S. counties, we aim to assess whether patterns exist that can help explain economic outcomes through the lens of higher education. While this study is limited to quantitative correlations, it can serve as a starting point for understanding how educational investment might influence local economies and where such investment may have the greatest impact.

Ultimately, **our goal is to test whether increasing educational attainment aligns with increased personal income** and to consider what this relationship implies for regional policy, resource allocation, and long-term economic development in the United States.


## Data Organization
Our dataset merges county-level income and education statistics from two primary sources: the Bureau of Economic Analysis (BEA) and the U.S. Department of Agriculture (USDA). It includes over 3,000 U.S. counties and focuses on recent data spanning 2015 to 2021.

The income data, sourced from the BEA (November 2022 release), includes:

- per_capita_personal_income_2019
- per_capita_personal_income_2020
- per_capita_personal_income_2021

These figures represent average income per person in each county, incorporating wages, investment returns, and government transfers.

The education data, from the USDA County-Level Dataset, includes both counts and percentages:

- associate_degree_numbers_2016_2020
- bachelor_degree_numbers_2016_2020
- associate_degree_percentage_2016_2020
- bachelor_degree_percentage_2015_2019

This dataset provides both the total number and the percentage of county residents who earned associate and bachelor’s degrees over specified time periods.

We also retained identifying information:

- county_FIPS, state, county

These columns identify the geographic location of each observation using the county’s FIPS code, state name, and county name.

These variables enable analysis of both absolute and relative educational attainment, allowing us to explore how income levels relate to education across different counties and regions. The multi-year averages smooth out short-term fluctuations and improve reliability. This structured dataset sets the foundation for statistical and spatial analysis of the link between economic prosperity and access to higher education.

## Exploratory Data Analysis
Research Question: How does education affect income at the county level in the United States?

To begin exploring the relationship between education and income, we conducted a thorough Exploratory Data Analysis (EDA) using a dataset containing U.S. county-level data on per capita personal income from 2019 to 2021, along with educational attainment rates for associate’s and bachelor’s degrees.

⸻

1. Data Overview and Cleaning

We started by reading the data from a CSV file hosted on GitHub and used the janitor package to clean and standardize column names. This is important to ensure consistent formatting for downstream analysis and modeling.
	•	Purpose: Standardized column names help prevent errors in processing and simplify referencing variables.
	•	Code used: clean_names() from the janitor package.

We also used glimpse() to inspect the structure of the dataset, which allowed us to quickly confirm the types and completeness of our variables.

📌 Insert: Screenshot or printout of glimpse(data) output

⸻

2. Variable Summary Table

We created a variable summary table to document each feature’s type (nominal, ratio) and a short description. This helps in understanding the dataset schema and planning which variables are suitable for modeling and visualization.

📌 Insert: Table summarizing variable types and descriptions (already included in the code)

⸻

3. Summary Statistics

Using the summary() function, we obtained descriptive statistics (mean, median, min, max, etc.) for all numerical variables.
	•	Purpose: This provides a general sense of distribution, central tendency, and variation in the data.

📌 Insert: Summary statistics output

⸻

4. Missing Values Check

We checked for missing values across all columns using colSums(is.na(data)).
	•	Purpose: Identifying and handling missing data is crucial to avoid bias or errors in modeling.

📌 Insert: Output showing missing value counts per column

⸻

5. Income Growth Over Time

We visualized how per capita income changed across 2019, 2020, and 2021 using boxplots.
	•	Purpose: To observe income distribution and trends over time, and to check for major economic shifts (e.g., pandemic impact).
	•	Insight: This helps contextualize education’s effect on income by tracking whether changes in income are consistent over time.

📊 Insert: Boxplot of income by year

⸻

6. Education Level Distributions

We plotted boxplots of associate and bachelor’s degree percentages.
	•	Purpose: To understand how educational attainment is distributed across counties, which is foundational for correlating with income.

📊 Insert: Boxplot comparing education percentages

⸻

7. Education vs. Income (Scatter Plots)

We created two scatter plots showing the relationship between:
	•	Associate Degree % and Income (2021)
	•	Bachelor’s Degree % and Income (2021)

Each included a linear regression trend line.
	•	Purpose: To visually assess the strength and direction of correlation between education level and income.
	•	Insight: A clear positive trend would suggest that higher education rates are associated with higher per capita income.

📊 Insert: Two scatter plots with linear trends

⸻

8. Correlation Matrix

We created a correlation matrix and heatmap for all numeric variables.
	•	Purpose: To quantitatively identify relationships between variables.
	•	Insight: This confirms whether our educational variables are significantly correlated with income, justifying their use in a predictive model.

📊 Insert: Correlation matrix heatmap

⸻

9. Linear Assumption & Distribution Checks

Using ggpairs, we evaluated distributions, outliers, and pairwise relationships between key variables.
	•	Purpose: To visually assess assumptions for linear modeling, including normality and linear relationships.
	•	Insight: Ensures that data meets the assumptions required for linear regression to be valid.

📊 Insert: GGPairs matrix showing histograms and scatter plots

⸻

10. Preprocessing for Modeling

Before training the model, we handled missing values via median imputation for numeric columns and dropped rows with missing categorical values. We also scaled numeric variables.
	•	Purpose: Preprocessing ensures that the model is trained on clean, normalized data, which improves accuracy and convergence.
	•	Insight: Proper preprocessing prevents data skew and enhances model interpretability.

📌 Insert: Note or table showing before/after stats for NA counts and feature scales

⸻

11. Feature Selection and Data Splitting

We selected per_capita_personal_income_2021 as the target variable and used the remaining features as predictors. We split the data into training and test sets (70/30).
	•	Purpose: Splitting ensures the model can be evaluated on unseen data, which is essential for estimating real-world performance.

📌 Insert: Table showing number of observations in train/test sets

⸻

12. Summary

Our EDA shows promising evidence of a positive relationship between education levels and income. These insights justify the development of a predictive model using education rates as key features.

⸻

## Main Observations and Conclusion
.

## Actionable Steps
probs figure out later

## Links
Youtube Video:
Google Colab:
