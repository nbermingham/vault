## Overview
**Homoscedasticity** is a key assumption in [[Regression]] analysis and [[Ordinary Least Squares (OLS)]] that assumes the variance of the residuals (errors) is constant across all levels of the independent variables. When homoscedasticity is present, the spread of the residuals is uniform, and model predictions are considered more reliable.

The opposite of homoscedasticity is **heteroscedasticity**, where the variance of residuals changes with the independent variables, potentially leading to inefficiencies and biased inferences.

---

## Key Characteristics

1. **Constant Variance**:
   - The residuals have the same variance across all levels of the independent variables.
2. **No Pattern in Residuals**:
   - When plotted, residuals should exhibit a random scatter without systematic patterns.
3. **Improved Efficiency**:
   - Homoscedasticity ensures that the [[Ordinary Least Squares (OLS)]] estimates are efficient and unbiased under the [[Gauss-Markov Theorem]].

---

## Importance

1. **Accurate Inference**:
   - Homoscedasticity is required for valid confidence intervals and hypothesis tests in regression.
2. **Unbiased Coefficient Estimates**:
   - While OLS can still provide unbiased estimates in the presence of heteroscedasticity, the standard errors may be incorrect, leading to invalid statistical inferences.

---

## Detection Methods

1. **Residual Plots**:
   - Plot residuals against predicted values or independent variables. A random scatter suggests homoscedasticity, while patterns indicate heteroscedasticity.
2. **Statistical Tests**:
   - **Breusch-Pagan Test**:
     - Tests for heteroscedasticity by examining the relationship between squared residuals and independent variables.
   - **White Test**:
     - A more general test for heteroscedasticity.
3. **Variance Analysis**:
   - Check whether the variance of residuals changes with independent variables.

---

## Consequences of Violating Homoscedasticity

1. **Invalid Hypothesis Tests**:
   - Standard errors are no longer reliable, leading to incorrect $t$-tests and $p$-values.
2. **Inefficient Estimates**:
   - Coefficients remain unbiased but are no longer the most efficient (minimum variance).
3. **Misleading Model Performance**:
   - Poor predictions and incorrect confidence intervals.

---

## Remedies for Heteroscedasticity

1. **Transformations**:
   - Apply log, square root, or other transformations to stabilize variance.
   - Example: Transform $y$ to $\log(y)$.
2. **Weighted Least Squares (WLS)**:
   - Adjusts the regression to give less weight to observations with higher variance.
3. **Robust Standard Errors**:
   - Use heteroscedasticity-consistent standard errors to correct inference issues.
4. **Feature Engineering**:
   - Add or modify independent variables to capture missing patterns.

---

## Example

Consider a regression model predicting income based on years of education:
1. Plot residuals against predicted income:
   - If residuals fan out as income increases, heteroscedasticity is present.
2. Apply a log transformation to income:
   - Stabilizes the variance and addresses heteroscedasticity.

---

## Related Topics

- [[Regression]]: Homoscedasticity is a key assumption in regression analysis.
- [[Ordinary Least Squares (OLS)]]: OLS assumes homoscedasticity for efficient and unbiased estimates.
- [[Gauss-Markov Theorem]]: Demonstrates the optimality of OLS under homoscedasticity.
- [[Heteroscedasticity]]: Understand the opposite phenomenon and its implications.
- [[Weighted Least Squares (WLS)]]: A solution for heteroscedasticity.

---

## Aliases
- Homoscedasticity
- Constant Variance Assumption

---

## Tags
#homoscedasticity #statistics #regression #OLS #gaussmarkov

---

## Links to Explore
- [[Regression]]: Understand how homoscedasticity affects regression models.
- [[Heteroscedasticity]]: Learn about its consequences and remedies.
- [[Ordinary Least Squares (OLS)]]: Explore how OLS relies on homoscedasticity for optimal estimates.
- [[Weighted Least Squares (WLS)]]: Discover an approach to handle heteroscedasticity.
- [[Gauss-Markov Theorem]]: Learn about the conditions under which OLS is optimal.