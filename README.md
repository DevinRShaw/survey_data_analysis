# Documentation for FEVS_trend_correlation_agencies.ipynb

This Python file provides an analysis of the Federal Employee Viewpoint Survey (FEVS) data, specifically focusing on trends and correlations among various agency metrics. The file uses `pandas`, `matplotlib`, `seaborn`, and `scipy` libraries to perform the analysis and visualize the results.

## Functions

### `barplot_select_column(df, selected_columns)`
This function takes a DataFrame `df` and a list of selected columns `selected_columns` as input. It calculates the mean values for the selected columns and creates a bar plot to visualize the mean values. The function also adds labels and a title to the plot.

### `test_normality(df)`
This function takes a DataFrame `df` as input. It performs the Shapiro-Wilk test for normality on the given data. If the p-value is greater than the significance level (0.05), it returns `True`, indicating that the data follows a normal distribution.

### `anova_test(df, variables)`
This function takes a DataFrame `df` and a list of variables `variables` as input. It creates a new DataFrame from the selected variables and performs ANOVA tests between each year and the next year. The function prints the F-statistic and p-value for each comparison and determines if there is a significant difference between the groups based on the p-value.

### `heatmap_years(df)`
This function takes a DataFrame `df` as input. It creates heatmaps to visualize the correlation between variables for each year. The function computes the correlation matrix, masks the upper triangle to focus on the lower triangle, and plots the heatmap using seaborn. It also prints a list of the variables sorted by their correlation strength, indicating their importance in the dataset.

### `agency_key_inspection(df)`
This function takes a DataFrame `df` as input. It plots key variables for each agency and each year. The function selects the rows corresponding to a specific agency, retrieves the scores for the key variables, and creates a bar plot for each year. The function repeats this process for each agency in the dataset.

### `key_score_plot(df)`
This function takes a DataFrame `df` as input. It plots the average scores for three key variables (Employee Engagement: Intrinsic Work Experience, New IQ: Empowered, and Global Satisfaction) for each agency and each year. The function calculates the average scores for each year and creates a line plot to visualize the trend. It also calculates the difference between the last two years' scores and prints the difference for each agency.

## Usage

The code starts by importing the necessary libraries and loading the FEVS dataset from a CSV file. It then defines several lists of columns representing different variables of interest.

Next, the code defines the aforementioned functions to perform various analyses and visualizations on the dataset.

The main part of the code consists of calling these functions to analyze and visualize the data. It includes:

1. Bar plots of the mean scores for each variable by year.
2. ANOVA tests to compare the average scores between consecutive years.
3. Heatmaps showing the correlations between variables for each year.
4. Bar plots of key variables for each agency and each year.
5. Line plots of the average scores for key variables for each agency and each year.

The code provides insights into the trends and correlations in the FEVS data, highlighting the importance of certain variables and their impact on employee engagement and job satisfaction.

To use this code, you need to have the `pandas`, `matplotlib`, `seaborn`, and `scipy` libraries installed. You also need to provide the path
