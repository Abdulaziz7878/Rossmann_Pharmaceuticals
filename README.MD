# Rossmann Pharmaceticals Sales Prediction

In this repository there is a project for predicting sales of Rossmann stores using machine learning and deep learning models.

## Table of Contents

- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [Data Preprocessing](#data-preprocessing)
- [Machine Learning Model](#machine-learning-model)
- [Deep Learning Model (LSTM)](#deep-learning-model-lstm)
- [Feature Importance & Confidence Interval](#feature-importance--confidence-interval)
- [Model Serialization](#model-serialization)
- [Conclusion](#conclusion)

## Introduction

This repository contains a comprehensive analysis of a sales prediction model utilizing machine learning techniques, specifically focusing on regression and time series forecasting. The analysis is based on the provided code and data files, which include training and testing datasets for sales data. The methodology encompasses data preprocessing, model training using Random Forest and LSTM (Long Short-Term Memory) networks, evaluation of model performance, and visualization of results.

## Project Structure

- `pridiction/`: Contains the pridicted datasets.
- `notebooks/`: Jupyter noteooks for each step.
- `README.md`: Project documentation.

## Data Preprocessing

1. **Loading Data**: Load store, train, and test datasets.
2. **Datetime Conversion**: Convert `Date` columns to datetime format.
3. **Label Encoding**: Encode categorical features.
4. **Feature Engineering**: Extract year, month, day, week, day of the year, and weekend indicator.
5. **Holiday Proximity**: Calculate days to/from holidays.
6. **Scaling**: Standardize features.

## Machine Learning Model

Using Random Forest Regressor:

Metrics: MSE, MAE, R-squared.

## Deep Learning Model (LSTM)

Steps:

1. **Time Series Preparation**: Transform to supervised learning format.
2. **LSTM Model**: Built with TensorFlow/Keras.
3. **Evaluation**: R-squared value and visual comparison.

## Feature Importance & Confidence Interval

Extract feature importance from Random Forest and estimate confidence intervals using bootstrap sampling.

## Model Serialization

Save models with timestamps for tracking:

```python

# Generate timestamp
timestamp = datetime.now().strftime('%Y-%m-%d-%H-%M-%S-%f')[:-3]  # Current timestamp in format YYYY-MM-DD-HH-MM-SS-MS

# Serialize and save the model
import joblib
model_filename = f'model_{timestamp}.pkl'

joblib.dump(pipeline, model_filename)

print(f'Model saved as {model_filename}')
```

## Conclusion

This project encapsulates a robust approach to predicting retail sales using machine learning techniques. The combination of Random Forest for initial predictions followed by LSTM for capturing temporal dynamics demonstrates a comprehensive methodology that leverages both regression analysis and time series forecasting. demonstrates predicting Rossmann store sales using both machine learning and deep learning. Steps include preprocessing, feature engineering, model building, evaluation, and serialization.
