# Regression Models for Stock Forecasting

This repository contains implementations of stock forecasting models and strategies in Python. The project is organized into two main folders:

1. **Linear Regression Model Folder**
   - `LinearRegression.py`: Contains the implementation of the linear and auto regression forecasting model with computed coefficient of determination of R².

   The Linear Regression (LR) model estimates regression coefficients (𝑏₀, 𝑏₁, …, 𝑏ᵣ) to create the function 𝑓(𝐱) = 𝑏₀ + 𝑏₁𝑥₁ + ⋯ + 𝑏ᵣ𝑥ᵣ, which reveals dependencies between inputs and output. It aims to make the predicted response 𝑓(𝐱ᵢ) as close as         possible to the actual response 𝑦ᵢ for each observation 𝑖 = 1, …, 𝑛. The differences 𝑦ᵢ - 𝑓(𝐱ᵢ) across all observations 𝑖 = 1, …, 𝑛 are residuals. Regression finds the best predicted weights by minimizing the sum of squared residuals (SSR) for all       observations 𝑖 = 1, …, 𝑛: SSR = Σᵢ(𝑦ᵢ - 𝑓(𝐱ᵢ))² using the ordinary least squares method.
