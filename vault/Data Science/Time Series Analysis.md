## Overview
**Time Series Analysis** is a statistical and computational method for analyzing and forecasting data points collected over time. It focuses on identifying patterns such as trends, [[Seasonality]], and cyclicality in temporal data to model and predict future values. Time series data appears in fields like [[Econometrics]], finance, weather forecasting, and machine learning.

---

## Key Components of Time Series

1. **Trend**:
   - Long-term movement in the data (e.g., a steady increase in stock prices).
2. **Seasonality**:
   - Regular, repeating patterns over a fixed period (e.g., higher sales during holidays).
3. **Cyclicality**:
   - Fluctuations without a fixed period, often influenced by economic or external conditions.
4. **Noise**:
   - Random variation or irregularities that cannot be explained by the model.

---

## Key Methods and Models

1. **[[Autoregressive Models (AR)]]**:
   - Predict future values using a linear combination of past values.
   - Example: [[ARIMA]] models.

2. **[[Moving Average Models (MA)]]**:
   - Use past forecast errors to predict future values.

3. **ARIMA** (Autoregressive Integrated Moving Average):
   - Combines AR and MA models with differencing to handle non-stationary data.

4. **[[Seasonal ARIMA (SARIMA)]]**:
   - Extends ARIMA by modeling seasonal patterns.

5. **[[Exponential Smoothing (ETS)]]**:
   - Captures trends and seasonality using weighted averages of past observations.

6. **[[State-Space Models]]**:
   - Include models like the [[Kalman Filter]] and dynamic linear models for flexible time series analysis.

7. **Machine Learning Methods**:
   - [[Recurrent Neural Networks (RNNs)]], [[Long Short-Term Memory (LSTM)|LSTMs]], and [[Transformers]] are used for complex, nonlinear time series tasks.

---

## Assumptions

1. **[[Stationarity]]**:
   - Many models assume that the statistical properties of the series (mean, variance) are constant over time.
2. **Autocorrelation**:
   - Observations are correlated with their past values.
3. **Linearity**:
   - Linear models like ARIMA assume linear relationships between time-lagged values.

---

## Applications

1. **Econometrics**:
   - Analyze and forecast GDP, inflation, unemployment, and other economic indicators.
2. **Finance**:
   - Predict stock prices, interest rates, and exchange rates.
3. **Weather Forecasting**:
   - Model temperature, rainfall, and other meteorological variables.
4. **Supply Chain**:
   - Forecast demand, inventory levels, and logistics patterns.
5. **Energy**:
   - Predict electricity usage, fuel demand, and renewable energy generation.

---

## Tools and Libraries

1. **Python**:
   - **Statsmodels**: [[ARIMA]], SARIMA, and time series diagnostics.
   - **Pandas**: Preprocessing and visualization.
   - **Prophet**: Automated trend and seasonality modeling.
   - **Scikit-learn**: Supervised learning for time series regression.
2. **R**:
   - `forecast` and `TSA` packages.
3. **Visualization Tools**:
   - [[Matplotlib]], Seaborn, and Plotly for time series plots.

---

## Key Metrics for Evaluation

1. **Mean Absolute Error (MAE)**:
   - Measures the average magnitude of errors.
2. **Mean Squared Error (MSE)**:
   - Penalizes larger errors more heavily.
3. **Root Mean Squared Error (RMSE)**:
   - Square root of MSE for interpretability.
4. **Mean Absolute Percentage Error (MAPE)**:
   - Expresses error as a percentage of observed values.

---

## Challenges

1. **Non-Stationarity**:
   - Many time series are not stationary and require transformations (e.g., differencing, detrending).
2. **[[Seasonality]]**:
   - Difficult to capture without explicit modeling (e.g., SARIMA or Fourier transforms).
3. **Missing Data**:
   - Gaps in time series can bias models.
4. **Noise**:
   - Random variations can obscure true patterns.

---

## Related Topics

- [[Stationarity]]: A critical assumption in many time series models.
- [[Autoregressive Models (AR)]]: Key component of ARIMA.
- [[Exponential Smoothing]]: Method for capturing trends and seasonality.
- [[Machine Learning]]: Applications of neural networks in time series.
- [[Forecasting]]: Broader application of time series analysis.

---

## Aliases
- Time Series
- Temporal Data Analysis
- Sequential Data Analysis

---

## Tags
#timeseries #statistics #forecasting #machinelearning #econometrics

---

## Links to Explore
- [[ARIMA]]: Explore a popular model for stationary and non-stationary data.
- [[Recurrent Neural Networks (RNNs)]]: Learn how neural networks handle sequential data.
- [[Stationarity]]: Understand its importance in time series modeling.
- [[Forecasting]]: Broader applications of time series analysis.
- [[Autoregressive Models (AR)]]: A key model in time series analysis.