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

## Data Analysis and Exploration
- Visualize location-based delay data using Plotly maps.
- Analyze factors affecting delays, including time of day, week, month, and weather conditions (if available).

## Data Visualizations
- Plot delay incidents using Plotly and analyze their impact.


