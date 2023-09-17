# Toronto TTC Bus Delay Prediction

## Overview
This project aims to predict bus delays in the Toronto Transit Commission (TTC) using various machine learning techniques. Predicting bus delays can help improve transit services and passenger experiences.

## Importing Libraries
- Pandas (`pd`)
- Numpy (`np`)
- Geopy's Nominatim for location data

## Raw Data Cleaning Process
- **Dataset:** [ttc-bus-delay-data-2022.csv](https://raw.githubusercontent.com/Sofiaanjum/TTC_Bus_Delay_Prediction/main/ttc-bus-delay-data-2022.csv)
- Create the target variable based on delay duration:
    - `0`: Delay within 5 mins (okay)
    - `1`: Delay more than 5 mins but eventually arrived (not good)
    - `2`: Never arrived (bad)
- Functions for cleaning:
    - `clean_columns`
    - `datetime_col`
    - `location_name`
    - `categorize` (custom function)

## Load Cleaned DataFrame
- Load the cleaned data from [cleaned_ttc.csv](https://github.com/Sofiaanjum/TTC_Bus_Delay_Prediction/blob/main/cleaned_ttc.csv).

## Constructing New DataFrame for Model Prediction

## Classification Model
- Utilize machine learning algorithms for classification, such as Random Forest Classifier.

## Time Series Analysis
- Perform time series analysis on the dataset:
  - Calculate rolling mean of 'MinDelay' column with a 7-day window.
  - Decompose the time series into trend, seasonal, and residual components.
  - Fit a Holt-Winters model to the time series with multiplicative seasonality.
  - Forecast future delays using the fitted model.

## Data Analysis and Exploration
- Visualize location-based delay data using Plotly maps.
- Analyze factors affecting delays, including time of day, week, month, and weather conditions (if available).

## Data Visualizations
- Plot delay incidents using Plotly and analyze their impact.

![Subway Delays](https://github.com/Sofiaanjum/TTC_Bus_Delay_Prediction/raw/main/image_01.jpg)
*Image: Subway line 1 and 2 experienced the majority of delays. [View Interactive Plot in Plotly](https://plotly.com/~sofia1501/1/)*

## Time Series Analysis
![Transportation Delay Incidents](https://github.com/Sofiaanjum/TTC_Bus_Delay_Prediction/raw/main/image_02.jpg)
*Image: There was a rise in transportation delay incidents during the second half of January, with a peak on January 19th, caused by a severe winter storm that significantly impacted Toronto's transportation systems*
