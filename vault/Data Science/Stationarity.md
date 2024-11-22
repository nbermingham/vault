---
aliases:
  - stationarity
---
## Overview
**Stationarity** is a fundamental concept in [[Time Series Analysis]] that assumes a time series' statistical properties, such as mean, variance, and autocorrelation, remain constant over time. Many models, including [[ARIMA]] and [[Autoregressive Models (AR)]], rely on the assumption of stationarity for accurate modeling and forecasting.

Stationarity simplifies the analysis of time series data by ensuring that the underlying patterns do not change over time.

---

## Types of Stationarity

1. **Strict Stationarity**:
   - A time series is strictly stationary if the joint distribution of any subset of observations is identical regardless of when they are observed.
   - Rarely used in practice due to strict mathematical requirements.

2. **Weak Stationarity (Second-Order Stationarity)**:
   - A time series is weakly stationary if:
     - The mean is constant over time.
     - The variance is constant over time.
     - The autocovariance depends only on the lag, not on time.

3. **Trend Stationarity**:
   - A series is trend stationary if the data can be made stationary by removing a deterministic trend.

4. **Difference Stationarity**:
   - A series is difference stationary if it becomes stationary after applying differencing.

---

## Key Properties of Stationary Time Series

1. **Constant Mean**:
   - The average value of the series does not change over time.

2. **Constant Variance**:
   - The spread of the series remains consistent over time.

3. **Autocovariance Depends Only on Lag**:
   - The relationship between observations depends on their relative lag, not the specific time.

---

## Detection Methods

1. **Visual Inspection**:
   - Plot the time series and check for visible trends or changing variance.

2. **Statistical Tests**:
   - **[[Augmented Dickey-Fuller (ADF) Test]]**:
     - Tests the null hypothesis that a series has a unit root (non-stationary).
   - **[[Kwiatkowski-Phillips-Schmidt-Shin (KPSS) Test]]**:
     - Tests the null hypothesis that a series is stationary.
   - **[[Phillips-Perron (PP) Test]]**:
     - An alternative to the ADF test for stationarity.

3. **[[Autocorrelation Function (ACF)]]**:
   - Stationary series exhibit a rapid decay in autocorrelation values.

4. **[[Rolling Statistics]]**:
   - Compute rolling mean and variance. If they change over time, the series is non-stationary.

---

## Remedies for Non-Stationarity

1. **[[Differencing]]**:
   - Subtract consecutive observations to remove trends and achieve stationarity.
   - Example: $Y_t' = Y_t - Y_{t-1}$.

2. **[[Detrending]]**:
   - Remove deterministic trends by subtracting the fitted trend line (e.g., linear regression).

3. **[[Transformation]]**:
   - Apply log, square root, or Box-Cox transformations to stabilize variance.

4. **[[Seasonal Adjustment]]**:
   - Remove seasonality using decomposition methods like [[Seasonal Decomposition of Time Series (STL)]].

---

## Applications

1. **Time Series Modeling**:
   - Models like [[ARIMA]], [[SARIMA]], and [[Autoregressive Models (AR)]] require stationary data.
2. **Forecasting**:
   - Accurate predictions rely on consistent statistical properties.
3. **Econometrics**:
   - Stationarity is critical for analyzing macroeconomic indicators like GDP and inflation.
4. **Signal Processing**:
   - Stationary signals simplify frequency domain analysis.

---

## Challenges

1. **Real-World Data is Rarely Stationary**:
   - Most time series exhibit trends, seasonality, or changing variance.
2. **Over-Differencing**:
   - Excessive differencing can remove valuable information, leading to underfitting.
3. **Mixed Stationarity**:
   - Some series may be stationary in certain intervals but not others.

---

## Related Topics

- [[Time Series Analysis]]: Stationarity is a foundational concept in analyzing temporal data.
- [[Autoregressive Models (AR)]]: Stationarity is a key assumption for AR models.
- [[ARIMA]]: Relies on stationarity after differencing non-stationary data.
- [[Seasonality]]: Seasonal patterns can affect stationarity and require adjustment.
- [[Trend Analysis]]: Identifying trends to achieve stationarity.

---

## Aliases
- Stationarity
- Stationary Time Series
- Time Series Stationarity

---

## Tags
#stationarity #timeseries #statistics #forecasting #econometrics

---

## Links to Explore
- [[Time Series Analysis]]: Learn how stationarity fits into time series modeling.
- [[ARIMA]]: Discover how differencing achieves stationarity for ARIMA models.
- [[Seasonal Decomposition of Time Series (STL)]]: Adjust for seasonality to achieve stationarity.
- [[Autoregressive Models (AR)]]: Explore stationary time series requirements for AR models.
- [[Augmented Dickey-Fuller Test]]: A common test for stationarity in time series data.