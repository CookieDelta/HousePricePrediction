﻿# Housing Price Prediction Project

The **Housing Price Prediction** project uses a dataset containing various features like geographical data, number of rooms, and income, with the target variable being the **median_house_value**.

## Data Exploration and Cleaning

The dataset includes 10 columns, with the key features being:

- `longitude`, `latitude`: Geographical coordinates.
- `housing_median_age`: Age of the house.
- `total_rooms`, `total_bedrooms`, `population`, `households`: Various features describing the number of rooms, bedrooms, and the size of the population in the area.
- `median_income`: Median income of the residents in the area.
- `ocean_proximity`: Categorical feature describing the proximity to the ocean.

Upon inspecting the data, we found that the `total_bedrooms` column had some missing values, which were dropped for cleaning. A quick check for null values revealed that there were no other issues.

## Data Pre-processing

- **Normalization**: Some features, such as `total_rooms`, `total_bedrooms`, `population`, and `households`, showed skewness. These were normalized using a logarithmic transformation.
  
- **One-Hot Encoding**: The `ocean_proximity` categorical feature was encoded using one-hot encoding, turning it into multiple binary columns.

## Feature Engineering

New features were created, such as:

- `bedroom_ratio`: The ratio of bedrooms to total rooms.
- `households_rooms`: The number of rooms per household.

These new features help capture more granular patterns in the data and improve model accuracy.

## Model Building and Evaluation

Several models were trained to predict the target variable, `median_house_value`:

1. **Linear Regression**: A simple baseline model provided an accuracy of around 66%.
   
2. **Random Forest Regressor**: A more complex model that achieved an accuracy of 80% on the test data.

3. **Hyperparameter Tuning**: Grid search was used to fine-tune the parameters of the Random Forest model, improving its performance further.

## Conclusion

This project demonstrated the process of exploring and cleaning real-world data, applying feature engineering techniques, and building predictive models. By using a Random Forest Regressor and fine-tuning its parameters, the model achieved a good performance, showcasing the importance of both data preprocessing and model selection in predictive modeling tasks.
