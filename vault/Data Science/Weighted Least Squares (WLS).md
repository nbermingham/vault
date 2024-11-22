## Overview
**Weighted Least Squares (WLS)** is a regression method that addresses heteroscedasticity in [[Ordinary Least Squares (OLS)]] models by assigning weights to observations based on the inverse of their variance. This ensures that observations with larger variance have less influence on the regression model, leading to more efficient and reliable parameter estimates.

WLS is commonly used in [[Econometrics]], [[Time Series Analysis]], and other fields where non-constant variance (heteroscedasticity) is present in the data.

---

## Formula

The objective function for WLS minimizes the weighted sum of squared residuals:
$$
J(\mathbf{w}) = \sum_{i=1}^N w_i \left( y_i - \hat{y}_i \right)^2
$$
Where:
- $w_i$: Weight for the $i$-th observation, often set as $w_i = \frac{1}{\sigma_i^2}$ (inverse of the variance of the residuals).
- $y_i$: Observed value of the dependent variable.
- $\hat{y}_i$: Predicted value of the dependent variable.
- $N$: Number of observations.

The WLS estimator for the coefficients is:
$$
\mathbf{w} = (\mathbf{X}^\top \mathbf{W} \mathbf{X})^{-1} \mathbf{X}^\top \mathbf{W} \mathbf{y}
$$
Where:
- $\mathbf{W}$: Diagonal matrix of weights with $w_i$ as the $i$-th diagonal element.
- $\mathbf{X}$: Design matrix of independent variables.
- $\mathbf{y}$: Vector of observed dependent variable values.

---

## Key Characteristics

1. **Addressing Heteroscedasticity**:
   - WLS adjusts for non-constant variance in residuals, ensuring efficient and reliable estimates.
2. **Weight Assignment**:
   - Observations with smaller variance are assigned higher weights, giving them more influence on the model.
3. **Generalization of OLS**:
   - WLS reduces to OLS when all weights are equal.

---

## Applications

1. **Econometrics**:
   - Used to model relationships in economic data where variability increases with the magnitude of the dependent variable (e.g., income and expenditure).
2. **Time Series Analysis**:
   - Addresses changing variance over time in [[Autoregressive Models (AR)]] and other time series models.
3. **Predictive Modeling**:
   - Mitigates the impact of heteroscedasticity in datasets with non-constant variance.

---

## Advantages

1. **Handles Heteroscedasticity**:
   - Produces efficient and reliable parameter estimates even when the residual variance is not constant.
2. **Improves Inference**:
   - Corrects standard errors, leading to valid $t$-tests, $p$-values, and confidence intervals.
3. **Flexible Weights**:
   - Can accommodate user-specified weights based on domain knowledge.

---

## Disadvantages

1. **Weight Estimation**:
   - Requires knowledge or estimation of the variance structure, which may not always be accurate.
2. **Sensitive to Weighting Errors**:
   - Incorrect weights can lead to biased or inefficient estimates.
3. **Computational Complexity**:
   - Slightly more complex than OLS due to the incorporation of weights.

---

## Example

Consider a dataset where the variance of residuals increases with the value of the dependent variable ($y$). Assign weights inversely proportional to the variance of each observation:
- For an observation with variance $\sigma_i^2$, set weight $w_i = \frac{1}{\sigma_i^2}$.
- Perform WLS regression using the weighted design matrix $\mathbf{W}$ to compute coefficients.

---

## Related Topics

- [[Ordinary Least Squares (OLS)]]: WLS generalizes OLS by incorporating weights.
- [[Homoscedasticity]]: WLS is used when the assumption of constant variance is violated.
- [[Heteroscedasticity]]: Understand the problem WLS is designed to address.
- [[Regression]]: A broader framework where WLS is applied.
- [[Time Series Analysis]]: Variance stabilization in time-dependent datasets.

---

## Aliases
- Weighted Least Squares
- WLS Regression

---

## Tags
#wls #regression #heteroscedasticity #econometrics #statistics

---

## Links to Explore
- [[Ordinary Least Squares (OLS)]]: Learn how WLS extends OLS for heteroscedastic data.
- [[Heteroscedasticity]]: Understand the key issue WLS addresses.
- [[Homoscedasticity]]: Compare WLS with scenarios where residual variance is constant.
- [[Time Series Analysis]]: Discover applications of WLS in time-dependent data.
- [[Regression]]: Explore WLS within the broader context of regression analysis.