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
To explore how income levels affect educational attainment across U.S. counties, we utilized a merged dataset that combines per capita personal income and educational statistics from authoritative federal sources. The primary sources include the Bureau of Economic Analysis (BEA) and the United States Department of Agriculture (USDA), offering detailed and consistent socioeconomic indicators. The dataset spans all U.S. counties and includes observations primarily from the period 2015 to 2021.

The income component of the dataset includes per capita personal income for the years 2019, 2020, and 2021, as provided by the BEA and released in November 2022. Per capita personal income is calculated by dividing total personal income in a county by its population. This measure accounts for wages, investment returns, government transfers, and other personal earnings. We focus primarily on 2021 to reflect recent economic conditions, while the additional years (2019 and 2020) provide temporal context for understanding changes in income levels due to macroeconomic shocks such as the COVID-19 pandemic.

The educational attainment component is drawn from the USDA’s County-Level Data Sets and encompasses both absolute numbers and percentages of residents who have attained associate’s and bachelor’s degrees. Specifically, associate degree data (both number and percentage) is aggregated from 2016 to 2020, while bachelor’s degree percentages are based on the 2015–2019 period. This multiyear aggregation enhances reliability by reducing volatility and accounting for delayed reporting or temporary fluctuations.

After data cleaning and integration, we retained the following columns for analysis:

- county_FIPS: A five-digit Federal Information Processing System code uniquely identifying each county
- state: Full name of the U.S. state in which the county resides
- county: Name of the county
- per_capita_personal_income_2019: County-level per capita income in 2019
- per_capita_personal_income_2020: County-level per capita income in 2020
- per_capita_personal_income_2021: County-level per capita income in 2021
- associate_degree_numbers_2016_2020: Total number of individuals in the county who attained an associate’s degree from 2016–2020
- bachelor_degree_numbers_2016_2020: Total number of individuals in the county who attained a bachelor’s degree from 2016–2020
- associate_degree_percentage_2016_2020: Percentage of the population with an associate’s degree (2016–2020)
- bachelor_degree_percentage_2015_2019: Percentage of the population with a bachelor’s degree (2015–2019)

This comprehensive dataset enables a robust analysis of the relationship between economic conditions and educational outcomes. In particular, we examine whether higher income levels correlate with increased rates of associate and bachelor’s degree attainment. By using both percentage-based and count-based indicators, we ensure that our results are not distorted by population size alone.

The geographic granularity of the dataset allows for regional comparisons—urban vs. rural, coastal vs. inland, and state-by-state trends. Such comparisons are vital in identifying spatial inequalities and educational access disparities. For instance, counties with high income but low educational attainment may reveal areas with systemic underinvestment in higher education, while counties with lower income but relatively high degree rates may reflect strong community college systems or state-level educational subsidies.

Ultimately, the structure of this dataset supports a wide range of statistical analyses, including correlation studies, multivariate regressions, and geospatial visualizations. These methods will help us determine not only whether income and education are related, but also how this relationship varies by geography and time.

## Exploratory Data Analysis
talk about EDA here. add graphs/picture and code later. make sure to make a header for each point u are talking about

## Main Observations and Conclusion
.

## Actionable Steps
probs figure out later

## Links
Youtube Video:
Google Colab:
