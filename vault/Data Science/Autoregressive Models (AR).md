## Overview
**Autoregressive Models (AR)** are a class of [[Time Series Analysis]] models that predict a variable based on its own past values. In an AR model, the current value of the time series is expressed as a linear combination of its previous values and a stochastic error term. These models are widely used in [[Econometrics]], [[Forecasting]], and other fields to analyze and predict temporal data.

---

## Formula

The general form of an AR model of order $p$ (denoted as AR($p$)) is:
$$
X_t = c + \sum_{i=1}^p \phi_i X_{t-i} + \epsilon_t
$$
Where:
- $X_t$: The value of the time series at time $t$.
- $c$: Constant term (intercept).
- $\phi_i$: Coefficients of the lagged values (autoregressive coefficients).
- $X_{t-i}$: Lagged values of the series (past observations).
- $\epsilon_t$: White noise (error term) with mean 0 and constant variance.

---

## Key Characteristics

1. **Lagged Dependencies**:
   - Models the relationship between the current value and its past values.
2. **Stationarity**:
   - AR models assume the time series is stationary (constant mean and variance over time).
3. **Order of the Model ($p$)**:
   - The number of lagged terms included in the model determines its complexity.

---

## Estimation Techniques

1. **Least Squares**:
   - Estimates the coefficients ($\phi_i$) by minimizing the sum of squared residuals.
2. **Maximum Likelihood Estimation (MLE)**:
   - Provides robust parameter estimates under certain assumptions.
3. **Yule-Walker Equations**:
   - A method based on the autocorrelation function (ACF) of the time series.

---

## Applications

1. **Forecasting**:
   - Predict future values of stock prices, weather patterns, or economic indicators.
2. **Econometrics**:
   - Analyze macroeconomic variables such as GDP, unemployment, or inflation rates.
3. **Signal Processing**:
   - Model and predict digital signals in engineering applications.

---

## Advantages

1. **Simplicity**:
   - Easy to understand and implement for stationary time series data.
2. **Interpretability**:
   - Coefficients provide insights into the relationship between past and current values.
3. **Effectiveness**:
   - Performs well for short-term forecasting in stationary datasets.

---

## Disadvantages

1. **Assumes Stationarity**:
   - Non-stationary time series require preprocessing (e.g., differencing).
2. **Limited to Linear Relationships**:
   - Cannot model complex, non-linear dependencies.
3. **Sensitivity to Outliers**:
   - Outliers can distort parameter estimates and predictions.

---

## Extensions

1. **ARMA Models**:
   - Combines AR with [[Moving Average Models (MA)]] to capture both autoregressive and moving average components.
2. **[[ARIMA]] Models**:
   - Extends ARMA by incorporating differencing to handle non-stationarity.
3. **Seasonal ARIMA (SARIMA)**:
   - Adds seasonal components to ARIMA for periodic time series.

---

## Example

For an AR(2) model:
$$
X_t = c + \phi_1 X_{t-1} + \phi_2 X_{t-2} + \epsilon_t
$$
- $X_t$ depends on its immediate past value ($X_{t-1}$) and the value before that ($X_{t-2}$).

If $c = 2$, $\phi_1 = 0.5$, $\phi_2 = -0.3$, and $\epsilon_t = 0.1$, the predicted value at time $t$ is:
$$
X_t = 2 + 0.5 X_{t-1} - 0.3 X_{t-2} + 0.1
$$

---

## Related Topics

- [[Time Series Analysis]]: Broader field that includes AR models.
- [[Moving Average Models (MA)]]: Complements AR models by modeling residuals.
- [[ARIMA]]: Combines AR and MA models with differencing for non-stationary data.
- [[Stationarity]]: A key assumption in AR models.
- [[Forecasting]]: A primary application of autoregressive models.

---

## Aliases
- Autoregressive Models
- AR Models

---

## Tags
#autoregressivemodels #timeseries #forecasting #econometrics #statistics

---

## Links to Explore
- [[Time Series Analysis]]: Explore the broader field of temporal data modeling.
- [[Moving Average Models (MA)]]: Learn about complementary models for residual analysis.
- [[ARIMA]]: Understand how AR models extend to handle non-stationary data.
- [[Stationarity]]: Discover techniques for testing and enforcing stationarity.
- [[Forecasting]]: Apply AR models to predict future trends.