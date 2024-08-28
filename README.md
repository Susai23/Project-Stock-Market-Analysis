# Predicting Stock Market Trends Using Machine Learning Models LSTM and Prophet

## Overview

This project focuses on predicting stock market trends using two machine learning models: Long Short-Term Memory (LSTM) networks and Prophet. The project is based on historical stock price data from Barclays PLC, covering the period from 2004 to 2024. The aim is to evaluate the effectiveness of LSTM and Prophet models in forecasting future stock prices.

## Table of Contents

- Project Description
- Features
- Data Collection and Preprocessing
- Modeling and Prediction
- Results
- Comparison of Models
- Requirements


## Project Description

The stock market is known for its volatility and the challenge it poses to accurate predictions. This project employs advanced machine learning techniques to predict future stock prices. We used an LSTM model to capture the sequential dependencies in stock price data, while the Prophet model is used for detecting seasonality and long-term trends.

## Features

- **LSTM Model**: Suitable for short-term price prediction by leveraging sequential patterns in the data.
- **Prophet Model**: Effective in identifying long-term trends and seasonality.
- **Data Preprocessing**: Involves normalization, handling missing values, and feature engineering with Simple Moving Averages (SMAs).
- **Comparative Analysis**: Performance comparison between LSTM and Prophet models using Root Mean Square Error (RMSE).

## Data Collection and Preprocessing

### Data Source

- The historical stock data for Barclays PLC was sourced from Yahoo Finance, covering daily stock prices from January 1, 2004, to June 28, 2024.

### Preprocessing Steps

- **Handling Missing Values**: Missing values in the stock prices were imputed using the mean of available data.
- **Normalization**: Data was normalized to a range of 0 to 1 using `MinMaxScaler`.
- **Feature Engineering**: Calculated 100-day and 200-day SMAs to smooth out short-term fluctuations and identify long-term trends.

## Modeling and Prediction

### LSTM Model

The LSTM model was chosen for its ability to learn from sequential data. The model was built with bidirectional layers to capture both forward and backward dependencies. The training involved optimizing the model using the Adam optimizer over 100 epochs.

### Prophet Model

Prophet, developed by Facebook, was used for time series forecasting. The model is particularly strong in handling missing data and capturing seasonality.

## Results

- **LSTM Model**: Achieved lower RMSE values on both training and test datasets, indicating strong short-term prediction performance.
- **Prophet Model**: While less accurate for short-term predictions, it provided valuable insights into long-term trends and seasonal effects.

## Comparison of Models

The LSTM model outperformed Prophet in predicting short-term stock prices due to its capacity to learn complex temporal dependencies. However, the Prophet model excelled in identifying broader trends and seasonality, making it a valuable tool for long-term forecasting.

## Requirements

To run this project, you need the following Python libraries:

```bash
pip install numpy pandas matplotlib yfinance tensorflow scikit-learn keras fbprophet
