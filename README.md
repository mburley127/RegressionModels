# Regression Models for Stock Forecasting

This repository contains implementations of stock forecasting models and strategies in Python. The project is organized into two main folders:

1. **Linear Regression Model Folder**
   - `LinearRegression.py`: Contains the implementation of the linear and auto regression forecasting model with computed coefficient of determination of R². <br/>

      The Linear Regression (LR) model estimates regression coefficients to create a function that describes the relationship between input variables and the output. The goal is to make the predicted response as close as possible to the actual response for each observation. The differences between the actual and predicted values across all observations are called residuals. The model finds the optimal weights by minimizing the sum of the squared residuals for all observations, using a method known as ordinary least squares.

2. **Autoregressive Integrated Moving Average Model Folder**
   - `AutoRegression.py`: Contains the implementation of the ARIMA forecasting model outlined below:

      The model begins with an ADF test to assess whether the time series data is stationary, meaning the statistical properties, such as mean and variance, remain constant over time. A p-value below 0.05 indicates that the series is stationary, leading to the rejection of the null hypothesis of a unit root. The script includes a function to perform the ADF test, visualize rolling statistics, and interpret the results. <br/>

      If the series is found to be non-stationary, it is essential to remove the trend to achieve stationarity. This is done by taking the logarithm of the series, which reduces the magnitude of values and stabilizes variance. The script computes a rolling average and standard deviation to help visualize and better understand the underlying trend and volatility in the data. <br/>

      The data is then split into training and testing sets to evaluate the model's forecasting accuracy. In this model, 90% of the data is used for training, with the remaining 10% reserved for testing. The script visualizes this split, clearly distinguishing between the training and testing periods. <br/>

      The ARIMA function automates the selection of the best ARIMA model parameters (p, d, q) by evaluating various combinations based on specified criteria. The model automatically determines whether the series requires differencing (d parameter) and adjusts the other parameters accordingly. The script provides the model summary and diagnostic plots. <br/>

      Once the optimal parameters are identified, an ARIMA model is constructed and fitted to the training data. The script then generates forecasts for the testing period, including confidence intervals to capture the range of possible outcomes. The forecast results are displayed, providing a detailed outlook for the series. <br/>
