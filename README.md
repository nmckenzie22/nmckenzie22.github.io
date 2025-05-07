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
To explore the question of how income levels affect educational attainment across U.S. counties, we utilized a merged dataset that combines per capita personal income data with educational attainment statistics. These data were sourced from two authoritative federal agencies: the Bureau of Economic Analysis (BEA) and the United States Department of Agriculture (USDA). The dataset includes values for all U.S. counties as of the year 2021, offering a detailed and granular view of socioeconomic and educational outcomes across the country.

The first component of our dataset—per capita personal income by county—was released in November 2022 by the BEA. This data measures the average income earned per person in a given county and is calculated by dividing the total personal income of the county by its population. Personal income includes wages, business income, dividends, rent, government benefits, and other sources of compensation. By using the 2021 data (the most recent available), we ensure our analysis reflects current economic realities. It is important to note that these income figures do not account for regional cost-of-living differences, but they do provide a useful baseline for comparing relative economic prosperity across counties.

The second component comes from the USDA’s County-Level Data Sets, which compile demographic and socioeconomic indicators across rural and urban counties. From this resource, we extracted statistics on educational attainment—specifically, the number and percentage of county residents who have earned an associate’s degree and a bachelor’s degree. These figures are aggregated over a 5-year period (2016–2020 for associate’s degree numbers and 2015–2019 for bachelor’s degree percentages), allowing for smoothing over short-term fluctuations and improving the robustness of the data.

After cleaning and merging the datasets, we retained the following key attributes for our analysis:
	•	county_FIPS: A unique identifier for each county (Federal Information Processing Standard code)
	•	state: Name of the state where the county is located
	•	county: Name of the county
	•	per_capita_personal_income_2021: Average personal income per individual in the county for 2021
	•	associate_degree_percentage_2016_2020: Percentage of county population holding an associate’s degree
	•	bachelor_degree_percentage_2015_2019: Percentage of county population holding a bachelor’s degree

This integrated dataset enables us to analyze the relationship between economic prosperity and educational attainment at the county level. Specifically, we are interested in assessing whether higher income levels are associated with higher percentages of residents completing associate and bachelor’s degrees. This analysis will help inform whether income disparities may be contributing to unequal access to or attainment of higher education.

Furthermore, by working with data at the county level, we can explore regional variations and identify patterns specific to urban, suburban, and rural areas. This spatial granularity is critical because income and education dynamics often differ significantly across geographic contexts. For example, counties with high income may cluster in metropolitan areas with greater access to higher education institutions, while lower-income rural counties may face structural barriers that limit educational opportunities.

Ultimately, this dataset provides a foundation for performing statistical analyses such as correlation, regression modeling, and geographic visualizations, which will allow us to draw meaningful conclusions about how income influences educational outcomes across the United States.

## Exploratory Data Analysis
talk about EDA here. add graphs/picture and code later. make sure to make a header for each point u are talking about

## Main Observations and Conclusion
.

## Actionable Steps
probs figure out later

## Links
Youtube Video:
Google Colab:
