## Overview
**ARIMA (Autoregressive Integrated Moving Average)** is a statistical model used for analyzing and forecasting [[Time Series Analysis]] data. It combines three components:
- **Autoregressive (AR)**: Incorporates the relationship between an observation and its previous values.
- **Integrated (I)**: Applies differencing to make the time series stationary.
- **Moving Average (MA)**: Models the relationship between an observation and past forecast errors.

ARIMA is particularly suited for univariate time series with trends and no seasonality. Seasonal variations are handled by its extension, [[SARIMA]].

---

## Key Components

1. **Autoregressive (AR) Component**:
   - Relates the current value to a linear combination of its past values.
   - Controlled by the parameter $p$, which specifies the number of lagged observations.

2. **Integrated (I) Component**:
   - Differencing the data removes trends to achieve stationarity.
   - Controlled by the parameter $d$, which specifies the number of differencing operations.

3. **Moving Average (MA) Component**:
   - Uses the relationship between an observation and past forecast errors.
   - Controlled by the parameter $q$, which specifies the size of the moving average window.

---

## ARIMA Model Notation

The model is denoted as ARIMA$(p, d, q)$:
- $p$: Order of the autoregressive component.
- $d$: Degree of differencing to achieve stationarity.
- $q$: Order of the moving average component.

---

## Assumptions

1. **Stationarity**:
   - The series should have a constant mean and variance over time. Differencing may be applied to make the series stationary.
2. **Linearity**:
   - ARIMA models linear relationships; non-linear patterns require other methods (e.g., [[LSTMs]]).
3. **No Seasonality**:
   - ARIMA assumes no seasonal patterns; for seasonality, use [[SARIMA]].

---

## Steps to Build an ARIMA Model

1. **Preprocessing**:
   - Plot the data and use visual inspection or statistical tests (e.g., [[Augmented Dickey-Fuller Test]]) to check stationarity.
   - Apply transformations (e.g., log or square root) to stabilize variance if necessary.
   - Apply differencing if the data is non-stationary.

2. **Parameter Selection**:
   - Use methods like the **Autocorrelation Function (ACF)** and **Partial Autocorrelation Function (PACF)** to estimate $p$ and $q$.
   - Experiment with $d$ based on the degree of non-stationarity.

3. **Model Fitting**:
   - Fit the ARIMA$(p, d, q)$ model using tools like Statsmodels or R's `forecast` package.

4. **Model Diagnostics**:
   - Check residual plots to ensure no patterns remain.
   - Use metrics like [[Akaike Information Criterion (AIC)]] or [[Bayesian Information Criterion (BIC)]] to compare models.

5. **Forecasting**:
   - Predict future values using the fitted ARIMA model.

---

## Advantages

1. **Flexibility**:
   - Captures trends and patterns in non-stationary time series.
2. **Simplicity**:
   - Well-suited for univariate forecasting without the need for external predictors.
3. **Strong Statistical Foundation**:
   - Provides interpretable parameters for analysis.

---

## Disadvantages

1. **Limited to Linear Relationships**:
   - Cannot model complex, non-linear dependencies.
2. **Manual Parameter Tuning**:
   - Selecting $p$, $d$, and $q$ requires expertise and experimentation.
3. **Not Robust to Missing Data**:
   - Requires complete datasets for reliable predictions.
4. **Seasonality Handling**:
   - Ineffective for seasonal data unless extended to [[SARIMA]].

---

## Applications

1. **Finance**:
   - Forecast stock prices, interest rates, or market trends.
2. **Econometrics**:
   - Model GDP, unemployment, or inflation rates.
3. **Sales and Demand Forecasting**:
   - Predict future demand for inventory or products.
4. **Energy**:
   - Forecast electricity usage or fuel consumption.

---

## Tools and Libraries

1. **Python**:
   - **Statsmodels**: Provides `SARIMAX` for ARIMA modeling.
   - **pmdarima**: Automates ARIMA parameter selection.
2. **R**:
   - `forecast` and `TSA` packages for ARIMA modeling.
3. **Visualization**:
   - Use [[Matplotlib]] or Plotly to analyze residuals and forecast results.

---

## Related Topics

- [[Time Series Analysis]]: Broader field that includes ARIMA as a key model.
- [[Stationarity]]: Critical for ARIMA's effectiveness.
- [[SARIMA]]: Extends ARIMA for seasonal data.
- [[Autoregressive Models (AR)]]: ARIMA incorporates autoregression as a component.
- [[Forecasting]]: A primary application of ARIMA.

---

## Aliases
- ARIMA
- Autoregressive Integrated Moving Average

---

## Tags
#ARIMA #timeseries #forecasting #statistics #machinelearning #econometrics

---

## Links to Explore
- [[Time Series Analysis]]: Explore how ARIMA fits into the broader context.
- [[SARIMA]]: Learn about modeling seasonal time series data.
- [[Stationarity]]: Understand why it’s essential for ARIMA modeling.
- [[Autoregressive Models (AR)]]: A key component of ARIMA.
- [[Forecasting]]: Discover how ARIMA is used for predictions.