# Air Passengers Time Series Analysis and Forecasting

## Overview
This project performs an in-depth time series analysis on the `AirPassengers.csv` dataset. The goal is to explore the data, check for stationarity, apply transformations, and build an ARIMA/SARIMA model to forecast future passenger numbers.

## Dataset
The dataset consists of monthly airline passenger counts from 1949 to 1960. It contains the following columns:
- **Month**: The month of the observation (YYYY-MM format)
- **#Passengers**: The total number of air passengers in that month

## Dependencies
To run this analysis, ensure you have the following Python libraries installed:
```bash
pip install pandas numpy statsmodels matplotlib seaborn
```

## Steps in Analysis

### 1. Importing Required Libraries
The necessary libraries are imported, including Pandas, NumPy, Statsmodels, Matplotlib, and Seaborn.

### 2. Loading and Preprocessing the Data
- The dataset is loaded using `pandas.read_csv()`.
- The `Month` column is set as the index for time series analysis.

### 3. Exploratory Data Analysis (EDA)
- A line plot of passenger counts over time is generated.
- Seasonal decomposition is performed using `seasonal_decompose` to extract trend, seasonality, and residual components.

### 4. Checking for Stationarity
- The Augmented Dickey-Fuller (ADF) test is conducted to check for stationarity.
- First and second-order differencing is applied to make the time series stationary if needed.
- ACF and PACF plots help determine AR and MA terms.

### 5. ARIMA Model Training
- An ARIMA/SARIMA model is defined with selected parameters.
- The model is fitted and its summary statistics are printed.

### 6. Forecasting Future Data
- The trained model is used to forecast the next 24 months.
- Forecasted values are plotted along with confidence intervals.

## Results and Insights
- The model successfully captures seasonality and trend components.
- The final forecast predicts air passenger growth over the next two years.

## Usage
To execute the analysis, simply run:
```python
python air_passengers_analysis.py
```
Ensure the dataset `AirPassengers.csv` is placed in the working directory.

## Future Enhancements
- Experiment with different ARIMA configurations.
- Apply alternative time series models such as LSTM.
- Incorporate external variables like economic indicators.

## Author
Developed by [Your Name / IIDST].
