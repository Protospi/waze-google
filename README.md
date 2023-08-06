# Project Name: Waze User Churn Prediction

## Introduction

This Git project aims to develop a machine learning model to predict user churn for Waze. The project has progressed with the completion of a project proposal and initial Python data inspection and organization on Waze's user data.

## Project Scope

The current task is focused on Exploratory Data Analysis (EDA) and data visualization. The team has received a request from Chidi Ga, the Senior Data Analyst, to perform EDA on the user data. The analysis will be presented in a Python notebook, showcasing the data structuring, cleaning, and various visualizations. Additionally, an executive summary will be prepared to keep stakeholders, including Harriet Hadzic, the Director of Data Analysis, informed about the progress.

## Dataset Information

The project utilizes a dataset named "waze_dataset.csv," which contains synthetic data created in partnership with Waze. The dataset consists of 14,999 rows, each representing a unique user, and contains 12 columns with the following information:

| Column Name           | Type  | Description                                                      |
|-----------------------|-------|------------------------------------------------------------------|
| label                 | obj   | Binary target variable ("retained" vs. "churned")                |
| sessions              | int   | Number of occurrences of a user opening the app during the month |
| drives                | int   | Number of occurrences of driving at least 1 km during the month  |
| device                | obj   | The type of device a user starts a session with                  |
| total_sessions        | float | A model estimate of the total number of sessions since onboarding|
| n_days_after_onboarding | int  | The number of days since a user signed up for the app             |
| total_navigations_fav1 | int   | Total navigations since onboarding to the user’s favorite place 1 |
| total_navigations_fav2 | int   | Total navigations since onboarding to the user’s favorite place 2 |
| driven_km_drives      | float | Total kilometers driven during the month                         |
| duration_minutes_drives | float | Total duration driven in minutes during the month                |
| activity_days         | int   | Number of days the user opens the app during the month           |
| driving_days          | int   | Number of days the user drives (at least 1 km) during the month  |

## Task Overview

1. Perform Exploratory Data Analysis (EDA) on the Waze user dataset.
2. Create data visualizations to better understand the data, including a box plot of the "drives" variable and a scatter plot of "drives" vs. "sessions."
3. Prepare an executive summary to communicate the analysis results to stakeholders.

## PACE Strategy

The PACE (Plan, Analyze, Construct, and Execute) strategy is a comprehensive framework designed to guide the development of the machine learning model for predicting user churn in the Waze project. The strategy involves a systematic approach to Plan the project, Analyze the dataset through Exploratory Data Analysis (EDA), Construct the necessary data visualizations and model, and Execute the project by preparing an executive summary to communicate the analysis results effectively to stakeholders. By following the PACE strategy, the team aims to achieve a well-structured and successful implementation of the user churn prediction model for Waze, ensuring valuable insights are communicated in a concise manner to all relevant stakeholders.

### Plan Stage

The Plan stage in the PACE strategy is a crucial initial step in the development of the user churn prediction model for Waze. During this stage, the team defines a clear roadmap and outlines the project scope and objectives. They identify the dataset, "waze_dataset.csv," and examine the data variables, understanding their types and descriptions. Moreover, the team defines the tasks to be accomplished, including performing Exploratory Data Analysis (EDA) and creating specific data visualizations as requested by the Senior Data Analyst and the Director of Data Analysis. By carefully planning the project's direction and tasks, the team ensures a structured and efficient approach, setting the foundation for successful analysis and model development.

- Define project objectives and scope: Clearly outline the goals and objectives of the user churn prediction model for Waze, along with the specific aspects of user data to be analyzed.

- Identify dataset and data variables: Select the dataset "waze_dataset.csv" for analysis and examine the data variables to understand their types and descriptions.

- Confirm analysis requirements: Review the request from Chidi Ga, the Senior Data Analyst, for specific analyses such as Exploratory Data Analysis (EDA) and data visualizations.

- Outline tasks and timeline: Create a detailed plan of the tasks to be completed, including conducting EDA, data cleaning, and visualization creation. Set a realistic timeline for each task to ensure project progress.

- Allocate roles and responsibilities: Assign roles to team members based on their expertise and strengths, ensuring each member knows their responsibilities during the project.

- Determine data preprocessing needs: Identify any data restructuring, conversion, or cleaning required to make the dataset suitable for analysis.

- Set up the development environment: Ensure that the required Python libraries and tools are installed and ready for use.

- Establish communication channels: Determine the communication methods among team members and stakeholders, and set up regular progress update meetings.

- Plan for documentation: Outline the format and content of the executive summary to be prepared, which will communicate the analysis results to stakeholders effectively.

- Assess potential risks and mitigation strategies: Identify potential challenges and risks that may arise during the project and develop strategies to address them effectively.

- Review and get approval: Present the plan to relevant stakeholders, seek feedback, and obtain approval before proceeding with the analysis.


### Analyse Stage

The Analyze stage in the PACE strategy plays a pivotal role in gaining a deeper understanding of the Waze user dataset and preparing it for further analysis. During this stage, the team addresses critical questions such as whether the data requires restructuring or conversion into usable formats. They thoroughly examine the dataset for any missing data in variables, which could potentially impact the accuracy of the analysis. Additionally, they assess the dataset's quality and perform data cleaning procedures to handle missing values appropriately. By meticulously analyzing the dataset and making necessary adjustments, the team ensures the data is ready for Exploratory Data Analysis (EDA) and data visualization, setting the stage for the subsequent stages of the project.

#### Data Eploration and Cleaning

In the given scenario of developing a machine learning model to predict user churn for Waze, the most applicable data columns are likely to be:

1. label: The binary target variable indicating whether a user has churned or retained, which is crucial for training the churn prediction model.
2. sessions: The number of times a user opens the app during the month, which could be an essential behavioral feature affecting churn.
3. drives: The number of occurrences of driving at least 1 km during the month, another behavioral feature that may correlate with user churn.
4. n_days_after_onboarding: The number of days since a user signed up for the app, which could be indicative of user engagement and retention.
5. driven_km_drives: The total kilometers driven during the month, which may provide insights into user activity and involvement.

Columns like device and total_navigations_fav1/fav2 may not directly contribute to predicting user churn and could be eliminated from the analysis, as they might not hold significant insights for the given scenario.

To check for missing data, the team can use functions like `isnull()` or `isna()` in Python to identify any missing values within the dataset. If missing data is present, the team can choose one of the following approaches to handle it:

1. Imputation: Replace missing values with a sensible estimate, such as the mean, median, or mode of the column.
2. Removal: Remove rows with missing data if the amount of missing data is insignificant and doesn't significantly affect the analysis.
3. Advanced methods: Use advanced techniques like interpolation or predictive modeling to impute missing values based on the relationships in other columns.

For detecting outliers, the team can utilize various statistical methods and visualization techniques like box plots, scatter plots, and z-scores. If outliers are identified and deemed influential, the team can handle them in the following ways:

1. Capping: Replace extreme outliers with the nearest reasonable value within a specific range to prevent them from skewing the analysis.
2. Transformation: Apply data transformations like logarithmic or power transformations to make the data less sensitive to outliers.
3. Removal: Remove outliers if they are deemed erroneous or significantly deviate from the general data distribution, but only if done with caution and after careful consideration of their impact on the analysis.

#### Data Structure

| Column                   | Non-Null Count | Dtype   |
|--------------------------|---------------|---------|
| ID                       | 14,999        | int64   |
| label                    | 14,299        | object  |
| sessions                 | 14,999        | int64   |
| drives                   | 14,999        | int64   |
| total_sessions           | 14,999        | float64 |
| n_days_after_onboarding  | 14,999        | int64   |
| total_navigations_fav1   | 14,999        | int64   |
| total_navigations_fav2   | 14,999        | int64   |
| driven_km_drives         | 14,999        | float64 |
| duration_minutes_drives  | 14,999        | float64 |
| activity_days            | 14,999        | int64   |
| driving_days             | 14,999        | int64   |
| device                   | 14,999        | object  |

The table provides a summary of the dataset columns, indicating the number of non-null values in each column and the corresponding data type (Dtype) for each attribute.

#### Data Summary

**Data Description:**

The dataset contains information related to user activity and driving behavior, with 14,999 rows and 11 columns. Below is a summary of the numerical attributes in the dataset:

| Attribute                 | Mean      | Std        | Min      | 25%       | 50%       | 75%       | Max        |
|---------------------------|-----------|------------|----------|-----------|-----------|-----------|------------|
| ID                        | 7499.00   | 4329.98    | 0.00     | 3749.50   | 7499.00   | 11248.50  | 14998.00   |
| sessions                  | 80.63     | 80.70      | 0.00     | 23.00     | 56.00     | 112.00    | 743.00     |
| drives                    | 67.28     | 65.91      | 0.00     | 20.00     | 48.00     | 93.00     | 596.00     |
| total_sessions            | 189.96    | 136.41     | 0.22     | 90.66     | 159.57    | 254.19    | 1216.15    |
| n_days_after_onboarding   | 1749.84   | 1008.51    | 4.00     | 878.00    | 1741.00   | 2623.50   | 3500.00    |
| total_navigations_fav1    | 121.61    | 148.12     | 0.00     | 9.00      | 71.00     | 178.00    | 1236.00    |
| total_navigations_fav2    | 29.67     | 45.39      | 0.00     | 0.00      | 9.00      | 43.00     | 415.00     |
| driven_km_drives          | 4039.34   | 2502.15    | 60.44    | 2212.60   | 3493.86   | 5289.86   | 21183.40   |
| duration_minutes_drives   | 1860.98   | 1446.70    | 18.28    | 835.99    | 1478.25   | 2464.36   | 15851.73   |
| activity_days             | 15.54     | 9.00       | 0.00     | 8.00      | 16.00     | 23.00     | 31.00      |
| driving_days              | 12.18     | 7.82       | 0.00     | 5.00      | 12.00     | 19.00     | 30.00      |

The data provides insights into user sessions, drives, total navigations, driven kilometers, and activity days. The mean, standard deviation, and quartile values offer valuable information about the central tendency and spread of the data. This summary serves as the foundation for further exploration and analysis of user behavior in this dataset.

### PACE: Construct     

In the Construct stage of the PACE strategy, we focus on building visualizations and preparing the data for analysis. We have explored the data, summarized its structure, and examined various numerical attributes. Now, we will address the presence of outliers and their impact on our analysis.

**Dealing with Outliers:**

Outliers are data points that significantly deviate from the overall pattern of the dataset. Identifying and handling outliers is crucial because they can heavily influence statistical measures and machine learning models. There are several ways to identify outliers, including:

1. **Boxplots:** Boxplots visually display the distribution of data and highlight potential outliers as individual points outside the whiskers.

2. **Z-Score:** Z-score measures the number of standard deviations a data point is away from the mean. Points with z-scores beyond a certain threshold are considered outliers.

3. **IQR (Interquartile Range):** IQR is the range between the first quartile (Q1) and the third quartile (Q3). Data points outside the range (Q1 - 1.5 * IQR) and (Q3 + 1.5 * IQR) are considered outliers.

4. **Visual Inspection:** Plotting histograms, scatter plots, or line graphs can help visually identify data points that lie far from the overall distribution.

The decision to keep or exclude outliers from future models depends on the context and objectives of the analysis. In some cases, outliers represent genuine anomalies or significant events, and excluding them could lead to loss of important information. On the other hand, outliers may be due to data entry errors or anomalies that don't reflect the underlying pattern. In such cases, excluding outliers might be appropriate to improve model performance and generalization.

As we proceed with our analysis, we will carefully evaluate the impact of outliers on different aspects of the data, such as statistical measures and model performance. Decisions regarding outlier handling will be made based on the goals of our analysis and the overall quality and reliability of the data.

### Data Visualization Strategy:

In the visualization stage of our analysis, we aim to gain deeper insights into the Waze dataset and effectively communicate our findings. Based on the data columns we have selected for our exploratory data analysis (EDA), we will utilize various data visualization types to understand and explain the data.

1. **Line Graph:** Line graphs will be helpful in visualizing trends and patterns over time or continuous variables. We can use line graphs to analyze the change in metrics such as sessions, drives, and navigations over different time periods.

2. **Bar Chart:** Bar charts are effective for comparing categorical data or discrete variables. We will use bar charts to visualize the distribution of categorical attributes like device and label, providing valuable insights into user preferences and behavior.

3. **Box Plot:** Box plots are useful for identifying the distribution, central tendency, and potential outliers in numerical variables. We will employ box plots to gain an understanding of variables like driven kilometers, duration of drives, and activity days.

4. **Histogram:** Histograms will be employed to depict the distribution of continuous variables such as sessions, drives, and navigations. They offer insights into the frequency and range of data values.

5. **Heat Map:** Heat maps are suitable for displaying the correlation between multiple variables. We may use heat maps to explore relationships between attributes like total sessions, total navigations, and duration minutes of drives.

6. **Scatter Plot:** Scatter plots are ideal for understanding the relationship between two continuous variables. We will utilize scatter plots to examine associations between variables like total sessions and total navigations.

7. **Geographic Map:** If the dataset contains geographic information, we can use geographic maps to visualize the distribution of activities in different regions or countries.

By employing a combination of these data visualization types, we will effectively explore and communicate the patterns, trends, and relationships present in the Waze dataset. Visualizations play a crucial role in making complex data more accessible and actionable, facilitating the decision-making process and generating valuable insights for further analysis.

*Note:* The visualizations can be found in the jupiter notebook on the repo

### Distributions

**Distribution of Sessions:**

- **Shape of the Distribution:** The distribution of sessions is also positively skewed to the right. This suggests that most users have a relatively low number of sessions, while a smaller group of users have a significantly higher number of sessions. The skewness indicates that there are relatively few users with a large number of sessions, leading to a long tail on the right side of the distribution.

- **Outliers:** Based on the interquartile range (IQR) * 1.5 rule, there are potential outliers in the dataset. The IQR is the range between the first quartile (Q1) and the third quartile (Q3). Any data points that fall below Q1 - 1.5 * IQR or above Q3 + 1.5 * IQR are considered outliers. In this case, since Q1 is 23 and Q3 is 112, the lower bound for potential outliers is -122.5, which is not applicable to sessions. However, the upper bound for potential outliers is 112 + 1.5 * 89 (the difference between Q3 and Q1), which is 247.5. Therefore, sessions with values greater than 247 could be considered potential outliers.

- **Minimum Sessions:** The minimum number of sessions recorded in the dataset is 0. This indicates that there are users who did not have any sessions during the observed time period.

- **Maximum Sessions:** The maximum number of sessions recorded in the dataset is 743. This indicates that some users had a significantly high number of sessions, which could be of interest for further investigation and analysis.

- **Mean and Median:** The mean number of sessions is 80.63, while the median is 56. The higher mean suggests that a few users with a relatively higher number of sessions are pulling the average up, causing a rightward shift in the distribution. The difference between the mean and the median further supports the presence of outliers or extreme values on the right side of the distribution.

**Distribution of Total Sessions:**

- **Shape of the Distribution:** The distribution of total sessions is also positively skewed to the right. This indicates that most users have a relatively low total number of sessions, while a smaller group of users have a significantly higher total number of sessions. The skewness suggests that there are relatively few users with a large total number of sessions, leading to a long tail on the right side of the distribution.

- **Outliers:** Based on the interquartile range (IQR) * 1.5 rule, there are potential outliers in the dataset. The IQR is the range between the first quartile (Q1) and the third quartile (Q3). Any data points that fall below Q1 - 1.5 * IQR or above Q3 + 1.5 * IQR are considered outliers. In this case, since Q1 is 90.66 and Q3 is 254.19, the lower bound for potential outliers is -235.5, which is not applicable to total sessions. However, the upper bound for potential outliers is 254.19 + 1.5 * 163.53 (the difference between Q3 and Q1), which is 504.66. Therefore, total sessions with values greater than 504 could be considered potential outliers.

- **Minimum Total Sessions:** The minimum total number of sessions recorded in the dataset is 0.22. This indicates that there are users who had very few or almost no sessions during the observed time period.

- **Maximum Total Sessions:** The maximum total number of sessions recorded in the dataset is 1216.15. This indicates that some users had a significantly high total number of sessions, which could be of interest for further investigation and analysis.

- **Mean and Median:** The mean total sessions is 189.96, while the median is 159.57. The higher mean suggests that a few users with a relatively higher total number of sessions are pulling the average up, causing a rightward shift in the distribution. The difference between the mean and the median further supports the presence of outliers or extreme values on the right side of the distribution.

**Distribution of Drives:**

- **Shape of the Distribution:** The distribution of drives is also positively skewed to the right. Similar to the sessions distribution, this indicates that most users have a relatively low number of drives, while a smaller group of users have a significantly higher number of drives. The skewness suggests that there are relatively few users with a large number of drives, leading to a long tail on the right side of the distribution.

- **Outliers:** Based on the interquartile range (IQR) * 1.5 rule, there are potential outliers in the dataset. The IQR is the range between the first quartile (Q1) and the third quartile (Q3). Any data points that fall below Q1 - 1.5 * IQR or above Q3 + 1.5 * IQR are considered outliers. In this case, since Q1 is 20 and Q3 is 93, the lower bound for potential outliers is -100.5, which is not applicable to drives. However, the upper bound for potential outliers is 93 + 1.5 * 73 (the difference between Q3 and Q1), which is 201.5. Therefore, drives with values greater than 201 could be considered potential outliers.

- **Minimum Drives:** The minimum number of drives recorded in the dataset is 0. This indicates that there are users who did not participate in any drives during the observed time period.

- **Maximum Drives:** The maximum number of drives recorded in the dataset is 596. This indicates that some users had a significantly high number of drives, which could be of interest for further investigation and analysis.

- **Mean and Median:** The mean number of occurrences of driving at least 1 km during the month is 67.28, while the median is 48. The higher mean suggests that a few users with a relatively higher number of drives are pulling the average up, causing a rightward shift in the distribution. The difference between the mean and the median further supports the presence of outliers or extreme values on the right side of the distribution.

**Distribution of Users' Number of Days After Onboarding:**

- **Shape of the Distribution:** The distribution of users' number of days after onboarding is fairly symmetrical, resembling a uniform distribution, indicated by the mean and median being relatively close in value. The data seems to be more evenly spread across the range of days after onboarding, without a strong skew to the right or left.

- **Outliers:** Based on the interquartile range (IQR) * 1.5 rule, there are no potential outliers in the dataset. The IQR is the range between the first quartile (Q1) and the third quartile (Q3). Any data points that fall below Q1 - 1.5 * IQR or above Q3 + 1.5 * IQR are considered outliers. In this case, since Q1 is 878 and Q3 is 2623.5, the lower bound for potential outliers is -1323.25, which is not applicable to the number of days after onboarding. Also, the upper bound for potential outliers is 2623.5 + 1.5 * 1745.5 (the difference between Q3 and Q1), which is 5352.75, which is also not applicable to the data.

- **Minimum Number of Days After Onboarding:** The minimum number of days after onboarding recorded in the dataset is 4. This indicates that there are users who signed up and started using the platform after only 4 days.

- **Maximum Number of Days After Onboarding:** The maximum number of days after onboarding recorded in the dataset is 3500. This indicates that some users might have signed up and started using the platform much later after onboarding.

- **Mean and Median:** The mean number of days after onboarding is 1749.84, while the median is 1741. This small difference between the mean and median further supports the uniform-like distribution, with minimal influence from extreme values.

**Distribution of Total Kilometers Driven During the Month:**

- **Shape of the Distribution:** The distribution of total kilometers driven during the month is positively skewed to the right. The mean (4039.34) is greater than the median (3493.86), indicating that there are relatively few users who have driven a significantly large number of kilometers, contributing to the long tail on the right side of the distribution. Most users have driven a lower number of kilometers.

- **Outliers:** Based on the interquartile range (IQR) * 1.5 rule, there might be potential outliers in the dataset. The IQR is the range between the first quartile (Q1) and the third quartile (Q3). Any data points that fall below Q1 - 1.5 * IQR or above Q3 + 1.5 * IQR are considered outliers. In this case, since Q1 is 2212.60 and Q3 is 5289.86, the lower bound for potential outliers is -1833.66, which is not applicable to the total kilometers driven. However, the upper bound for potential outliers is 5289.86 + 1.5 * 3077.26 (the difference between Q3 and Q1), which is 9795.98. Therefore, total kilometers driven with values greater than 9795.98 could be considered potential outliers.

- **Minimum Total Kilometers Driven:** The minimum total kilometers driven recorded in the dataset is 60.44. This indicates that there are users who have driven a relatively small distance during the observed time period.

- **Maximum Total Kilometers Driven:** The maximum total kilometers driven recorded in the dataset is 21183.40. This indicates that some users have driven a significantly long distance during the observed time period.

**Distribution of Total Duration of Minutes Driven During the Month:**

- **Shape of the Distribution:** The distribution of total duration of minutes driven during the month is also positively skewed to the right. The mean (1860.98) is greater than the median (1478.25), indicating that there are relatively few users who have driven for a significantly longer duration, contributing to the long tail on the right side of the distribution. Most users have driven for a shorter duration.

- **Outliers:** Based on the interquartile range (IQR) * 1.5 rule, there might be potential outliers in the dataset. The IQR is the range between the first quartile (Q1) and the third quartile (Q3). Any data points that fall below Q1 - 1.5 * IQR or above Q3 + 1.5 * IQR are considered outliers. In this case, since Q1 is 835.99 and Q3 is 2464.36, the lower bound for potential outliers is -1087.49, which is not applicable to the total duration of minutes driven. However, the upper bound for potential outliers is 2464.36 + 1.5 * 1628.37 (the difference between Q3 and Q1), which is 4984.52. Therefore, total duration of minutes driven with values greater than 4984.52 could be considered potential outliers.

- **Minimum Total Duration of Minutes Driven:** The minimum total duration of minutes driven recorded in the dataset is 18.28. This indicates that there are users who have driven for a relatively short duration during the observed time period.

- **Maximum Total Duration of Minutes Driven:** The maximum total duration of minutes driven recorded in the dataset is 15851.73. This indicates that some users have driven for a significantly longer duration during the observed time period.

**Distribution of Number of Days Users Open the App During the Month:**

- **Shape of the Distribution:** The distribution of the number of days users open the app during the month appears to be approximately symmetric. The mean (15.54) is quite close to the median (16.00), indicating that the data is relatively evenly distributed around the central value. This suggests that a substantial number of users open the app for a similar number of days during the month.

- **Outliers:** Based on the interquartile range (IQR) * 1.5 rule, there are no potential outliers in the dataset. The IQR is the range between the first quartile (Q1) and the third quartile (Q3). Any data points that fall below Q1 - 1.5 * IQR or above Q3 + 1.5 * IQR are considered outliers. In this case, since Q1 is 8 and Q3 is 23, the lower bound for potential outliers is -15.5, which is not applicable to the number of days users open the app. Similarly, the upper bound for potential outliers is 23 + 1.5 * 15 (the difference between Q3 and Q1), which is 45.5, and there are no observations exceeding this threshold.

- **Minimum Number of Days Users Open the App:** The minimum number of days users open the app during the month is 0. This indicates that some users did not open the app at all during the observed time period.

- **Maximum Number of Days Users Open the App:** The maximum number of days users open the app during the month is 31. This indicates that some users open the app every day during the observed time period.

**Distribution of Number of Days Users Drive at Least 1 km During the Month:**

- **Shape of the Distribution:** The distribution of the number of days users drive at least 1 km during the month appears to be relatively symmetric. The mean (12.18) is close to the median (12.00), suggesting that the data is evenly distributed around the central value. This indicates that a significant number of users drive on a similar number of days during the month.

- **Outliers:** Based on the interquartile range (IQR) * 1.5 rule, there are no potential outliers in the dataset. The IQR is the range between the first quartile (Q1) and the third quartile (Q3). Any data points that fall below Q1 - 1.5 * IQR or above Q3 + 1.5 * IQR are considered outliers. In this case, since Q1 is 5 and Q3 is 19, the lower bound for potential outliers is -17.0, which is not applicable to the number of days users drive at least 1 km. Similarly, the upper bound for potential outliers is 19 + 1.5 * 14 (the difference between Q3 and Q1), which is 40.5, and there are no observations exceeding this threshold.

- **Minimum Number of Days Users Drive:** The minimum number of days users drive at least 1 km during the month is 0. This indicates that there are users who did not drive at all during the observed time period.

- **Maximum Number of Days Users Drive:** The maximum number of days users drive at least 1 km during the month is 30. This indicates that some users drive every day during the observed time period.

**Distribution of Device Types:**

The pie chart displays the distribution of device types used by users in the dataset. It is evident that the majority of users, comprising approximately 66.7% of the sample, use iPhones. On the other hand, Android users make up the remaining 33.3% of the data. This distribution indicates that there are nearly twice as many iPhone users as there are Android users in the dataset.

**Distribution of Churned and Retained Users:**

The pie chart illustrates the distribution of users between those who have churned and those who have been retained. It is evident that the majority of users, representing approximately 82% of the sample, have been retained. On the other hand, only around 18% of the users have churned. This distribution indicates that less than 18% of the users churned, while the remaining 82% have been retained.

### Outliers

In the data exploration process, it was observed that many variables in the dataset have outliers. These outliers are not considered data entry errors but are present due to the right-skewed nature of the distributions. Depending on the specific analysis or modeling tasks, it may be beneficial to handle these outliers by imputing them with more reasonable values.

To address this, a function was implemented that calculates the 95th percentile of a given column and then replaces any values greater than the 95th percentile with the value at the 95th percentile. This approach helps to bring extreme values closer to the bulk of the data distribution, providing a more balanced and representative dataset for further analysis.

By applying this imputation technique to relevant columns such as 'sessions', 'drives', 'total_sessions', 'driven_km_drives', and 'duration_minutes_drives', we ensure that the data remains more consistent and suitable for subsequent analyses. It is important to consider the context and purpose of the analysis when deciding how to handle outliers, and this percentile-based imputation provides a useful approach for this dataset.

**Describe method after the cleaning**

|               | sessions | drives | total_sessions | driven_km_drives | duration_minutes_drives |
|---------------|---------|--------|----------------|------------------|-------------------------|
| count         | 14999   | 14999  | 14999          | 14999            | 14999                   |
| mean          | 76.57   | 64.06  | 184.03         | 3939.63          | 1789.65                 |
| std           | 67.30   | 55.31  | 118.60         | 2216.04          | 1222.71                 |
| min           | 0.00    | 0.00   | 0.22           | 60.44            | 18.28                   |
| 25%           | 23.00   | 20.00  | 90.66          | 2212.60          | 835.99                  |
| 50%           | 56.00   | 48.00  | 159.57         | 3493.86          | 1478.25                 |
| 75%           | 112.00  | 93.00  | 254.19         | 5289.86          | 2464.36                 |
| max           | 243.00  | 201.00 | 454.36         | 8889.79          | 4668.90                 |


## Executive Summary:

Our exploratory data analysis (EDA) of the Waze dataset has revealed valuable insights that can provide essential guidance to stakeholders. Through a comprehensive examination of various variables, we have gained a deeper understanding of user behavior, app engagement, and churn rates, shedding light on critical aspects for Waze's growth and success.

Key Findings:

1. Churn Rate by App Usage: The churn rate is notably higher for users who had little or no activity on Waze during the last month. As usage frequency increased, the likelihood of churning decreased significantly. For users who did not use the app at all in the last month, the churn rate reached 40%, while no users who used the app for 30 days churned. This observation indicates the importance of engaging users consistently to retain their loyalty.

2. Session and Drive Distributions: Both sessions and drives exhibit right-skewed distributions, with the majority of users having relatively low values, and a smaller group with significantly higher activity. This suggests that while most users engage with Waze moderately, a few power users contribute significantly to the overall app activity.

3. Impact of Driving Days: Users who have more driving days tend to have more sessions, indicating a positive correlation between app engagement and driving frequency. This insight underscores the value of Waze as a dependable navigational companion for regular drivers.

4. Outlier Handling: Addressing outliers is crucial to maintain data integrity. We implemented a technique to impute outlying values based on the 95th percentile of each variable, which allowed us to mitigate the influence of extreme values and maintain a balanced dataset.

5. Device Preference: The dataset primarily consists of iPhone users, nearly twice as many as Android users. This insight can inform Waze's development and marketing strategies, focusing on providing an optimal experience for the iPhone user base.

Conclusion:

Our EDA provides essential guidance for Waze's strategic decision-making. By understanding user behavior, identifying engagement patterns, and addressing churn rates, Waze can tailor its services to meet user expectations more effectively. The key takeaway is to focus on engaging users consistently through the app's features and offering a seamless navigation experience, thereby enhancing user loyalty and satisfaction. Moreover, as we continue to explore the dataset, additional valuable insights may arise, enabling Waze to stay at the forefront of the navigation app market.

Questions: 

1. What types of distributions did you notice in the variables? What did this tell you about the data?
    
    Nearly all the variables were either very right-skewed or uniformly distributed. For the right-skewed distributions, this means that most users had values in the lower end of the range for that variable. For the uniform distributions, this means that users were generally equally likely to have values anywhere within the range for that variable.

2. Was there anything that led you to believe the data was erroneous or problematic in any way?

    Most of the data was not problematic, and there was no indication that any single variable was completely wrong. However, several variables had highly improbable or perhaps even impossible outlying values, such as driven_km_drives. Some of the monthly variables also might be problematic, such as activity_days and driving_days, because one has a max value of 31 while the other has a max value of 30, indicating that data collection might not have occurred in the same month for both of these variables.

3. Did your investigation give rise to further questions that you would like to explore or ask the Waze team about?

    Yes. I'd want to ask the Waze data team to confirm that the monthly variables were collected during the same month, given the fact that some have max values of 30 days while others have 31 days. I'd also want to learn why so many long-time users suddenly started using the app so much in just the last month. Was there anything that changed in the last month that might prompt this kind of behavior?

4. What percentage of users churned and what percentage were retained?
    
    Less than 18% of users churned, and ~82% were retained.

5. What factors correlated with user churn? How?

    Distance driven per driving day had a positive correlation with user churn. The farther a user drove on each driving day, the more likely they were to churn. On the other hand, number of driving days had a negative correlation with churn. Users who drove more days of the last month were less likely to churn.

6. Did newer uses have greater representation in this dataset than users with longer tenure? How do you know?

    No. Users of all tenures from brand new to ~10 years were relatively evenly represented in the data. This is borne out by the histogram for n_days_after_onboarding, which reveals a uniform distribution for this variable.