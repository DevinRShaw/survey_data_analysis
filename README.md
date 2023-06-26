# FEVS Analysis

This repository contains an analysis of the Federal Employee Viewpoint Survey (FEVS) data. The analysis is performed in the `FEVS_analysis.ipynb` Jupyter Notebook file.

## Dataset
The FEVS dataset used for this analysis is stored in the `full_FEVS_prototype.csv` file. The dataset includes responses from multiple years, with each year represented by a separate column in the dataset.

## Analysis Framework
The analysis starts by defining a framework for analyzing the data. The framework includes:

- Lists of related variables ordered by year
- Functions for mass visualization, such as creating bar plots of yearly changes in a variable
- Functions for conducting ANOVA tests to compare average scores between different years
- Functions for testing the normality of variables

## Initial Insights
The analysis begins with the visualization of yearly changes in the variables. Some initial insights from the bar plots include:

- There is a trend of increasing scores that tapers off and possibly lowers after 2020.
- This trend may be attributed to the changes in work patterns due to the COVID-19 pandemic.

## ANOVA to Compare Average Scores between Different Years
ANOVA (Analysis of Variance) is used as a statistical tool to compare the average scores between different years. The following steps are performed:

1. Hypothesis formulation: The null hypothesis assumes that the average scores are the same across all years, while the alternative hypothesis assumes that the average scores are different across at least two years.
2. Data organization: Each year is represented by a separate column in the dataset, with the scores recorded in the respective columns.
3. Assumption checking: Preliminary checks are performed to evaluate the assumptions of ANOVA, such as the independence of observations, normality of data within each group, and homogeneity of variances across groups.
4. ANOVA procedure: ANOVA tests are conducted to determine if there are significant differences in the average scores across the years.
5. Result interpretation: If the p-value is below the predetermined significance level (e.g., α = 0.05), the null hypothesis is rejected, indicating significant differences in the average scores between at least two years. Post-hoc tests, such as Tukey's HSD test, can be performed to identify specific years with significantly different scores.

## Insights from ANOVA
The analysis of the FEVS data reveals the following insights:

- There is a trend showing a subtle increase in survey scores from 2015 to 2018, followed by a plateau and a general increase in scores in 2020. However, scores decrease in 2022.
- ANOVA tests indicate significant differences between years of increase or decrease in scores, while plateau years do not show significant differences.
- The cause of this trend could be attributed to various factors, which may be explored through policy analysis across government agencies, specifically NOAA.
- The decrease in scores in 2022 may be related to the impact of COVID-19 and changes in policies affected by the pandemic. Further analysis can be conducted to identify specific policies and strategies to improve scores.

For detailed analysis and code implementation, please refer to the `FEVS_analysis.ipynb` notebook in this repository.

Please note that this is a summary of the analysis and further exploration and interpretation of the data may provide additional insights.
