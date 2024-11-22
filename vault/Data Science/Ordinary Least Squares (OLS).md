## Overview
**Ordinary Least Squares (OLS)** is a fundamental method in [[Regression]] analysis used to estimate the parameters of a linear model. It minimizes the sum of the squared differences between the observed values and the predicted values of the dependent variable. OLS is widely used in [[Machine Learning]], [[Econometrics]], and statistics due to its simplicity and interpretability.

---

## Formula

The objective of OLS is to minimize the following cost function:
$$
J(\mathbf{w}) = \sum_{i=1}^N \left( y_i - \hat{y}_i \right)^2
$$
Where:
- $y_i$: Observed value of the dependent variable for the $i$-th sample.
- $\hat{y}_i$: Predicted value, $\hat{y}_i = \mathbf{x}_i^\top \mathbf{w}$.
- $\mathbf{w}$: Vector of coefficients (parameters).
- $N$: Number of observations.

The optimal coefficients are given by:
$$
\mathbf{w} = (\mathbf{X}^\top \mathbf{X})^{-1} \mathbf{X}^\top \mathbf{y}
$$
Where:
- $\mathbf{X}$: Design matrix of independent variables.
- $\mathbf{y}$: Vector of observed dependent variable values.

---

## Assumptions

1. **Linearity**:
   - The relationship between independent variables ($\mathbf{X}$) and the dependent variable ($y$) is linear.
2. **No Multicollinearity**:
   - Independent variables are not perfectly correlated (see [[Multicollinearity]]).
3. **[[Homoscedasticity]]**:
   - Constant variance of the error terms.
4. **No [[Autocorrelation]]**:
   - Error terms are not correlated with each other.
5. **Normality of Errors**:
   - Residuals are normally distributed (important for hypothesis testing).

---

## Properties

1. **Best Linear Unbiased Estimator (BLUE)**:
   - Under the [[Gauss-Markov Theorem]], OLS produces the best linear unbiased estimates of the coefficients when the assumptions are satisfied.
2. **Interpretability**:
   - Coefficients represent the expected change in the dependent variable for a one-unit change in the independent variable, holding others constant.
3. **Sensitivity**:
   - OLS is sensitive to outliers and multicollinearity.

---

## Applications

1. **Econometrics**:
   - Estimate relationships between economic indicators (e.g., income and expenditure).
2. **Machine Learning**:
   - Serve as a baseline model for [[Linear Regression]] tasks.
3. **Forecasting**:
   - Predict future values of dependent variables based on independent variables.

---

## Advantages

1. **Simplicity**:
   - Easy to implement and interpret.
2. **Efficiency**:
   - Computationally inexpensive for small to medium-sized datasets.
3. **Theoretical Foundation**:
   - Provides a closed-form solution with well-defined properties under the assumptions.

---

## Disadvantages

1. **Assumption Sensitivity**:
   - Violations of assumptions (e.g., heteroscedasticity, multicollinearity) can lead to biased or inefficient estimates.
2. **Outliers**:
   - Highly sensitive to extreme values.
3. **Scalability**:
   - Computing the matrix inverse becomes expensive for very large datasets.

---

## Example

Consider a simple linear regression model:
$$
y = w_0 + w_1 x + \epsilon
$$
Given data points $(x, y) = \{(1, 2), (2, 3), (3, 5)\}$:
1. Construct the design matrix $\mathbf{X}$:
   $$
   \mathbf{X} =
   \begin{bmatrix}
   1 & 1 \\
   1 & 2 \\
   1 & 3
   \end{bmatrix}
   $$
2. Compute $\mathbf{w}$:
   $$
   \mathbf{w} = (\mathbf{X}^\top \mathbf{X})^{-1} \mathbf{X}^\top \mathbf{y}
   $$
   Resulting in $w_0 = 1$, $w_1 = 1$.

The final model is:
$$
\hat{y} = 1 + x
$$

---

## Related Topics

- [[Linear Regression]]: OLS is the standard method for fitting linear regression models.
- [[Multicollinearity]]: Can distort OLS estimates if present.
- [[R-Squared]]: Measures the goodness-of-fit of OLS models.
- [[Regularization]]: Extends OLS with penalty terms (e.g., [[Lasso Regression]], [[Ridge Regression]]).
- [[Gauss-Markov Theorem]]: Establishes the optimality of OLS estimates under certain conditions.

---

## Aliases
- Ordinary Least Squares
- OLS Regression
- Least Squares Regression

---

## Tags
#OLS #linearregression #statistics #econometrics #machinelearning

---

## Links to Explore
- [[Linear Regression]]: Learn how OLS fits linear models.
- [[Multicollinearity]]: Understand how it impacts OLS estimates.
- [[Regularization]]: Explore techniques to improve OLS for high-dimensional data.
- [[R-Squared]]: Assess the performance of OLS models.
- [[Gauss-Markov Theorem]]: Discover the conditions under which OLS is optimal.