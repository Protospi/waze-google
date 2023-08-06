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

### Plan Step

The Plan stage in the PACE strategy is a crucial initial step in the development of the user churn prediction model for Waze. During this stage, the team defines a clear roadmap and outlines the project scope and objectives. They identify the dataset, "waze_dataset.csv," and examine the data variables, understanding their types and descriptions. Moreover, the team defines the tasks to be accomplished, including performing Exploratory Data Analysis (EDA) and creating specific data visualizations as requested by the Senior Data Analyst and the Director of Data Analysis. By carefully planning the project's direction and tasks, the team ensures a structured and efficient approach, setting the foundation for successful analysis and model development.