## Overview
**Heteroscedasticity** occurs when the variance of residuals (errors) in a regression model is not constant across all levels of the independent variables. This violates the assumption of [[Homoscedasticity]] in [[Ordinary Least Squares (OLS)]], leading to inefficient coefficient estimates and invalid statistical inferences.

Heteroscedasticity is common in real-world datasets, particularly when the dependent variable exhibits greater variability as its predicted value increases or decreases.

---

## Key Characteristics

1. **Non-Constant Variance**:
   - The residuals' spread changes with the levels of independent variables or predicted values.
2. **Patterns in Residual Plots**:
   - Residuals often show a funnel shape, clustering, or other patterns when plotted against predicted values or independent variables.

---

## Causes

1. **Scale Effects**:
   - As the magnitude of the dependent variable increases, variability may naturally grow (e.g., income variability grows with income level).
2. **Omitted Variables**:
   - Excluding important predictors can cause residuals to exhibit heteroscedasticity.
3. **Data Transformations**:
   - Poorly chosen transformations of variables can lead to heteroscedasticity.
4. **Structural Changes**:
   - Heteroscedasticity can result from changes in population subgroups (e.g., different variance for different income brackets).

---

## Consequences

1. **Invalid Hypothesis Testing**:
   - Standard errors of the coefficients are incorrect, leading to unreliable $t$-tests, $p$-values, and confidence intervals.
2. **Inefficient Estimates**:
   - Coefficients remain unbiased, but they are no longer efficient, meaning higher variance than necessary.
3. **Misleading Model Evaluation**:
   - Predictions and performance metrics may not be reliable.

---

## Detection Methods

1. **Residual Plots**:
   - Plot residuals against predicted values or independent variables. A clear pattern or funnel shape indicates heteroscedasticity.
2. **Statistical Tests**:
   - **[[Breusch-Pagan Test]]**:
     - Detects heteroscedasticity by examining the relationship between squared residuals and independent variables.
   - **[[White Test]]**:
     - A more general test that does not assume a specific pattern of heteroscedasticity.
3. **Variance Analysis**:
   - Examine whether variance changes significantly across different groups or levels of an independent variable.

---

## Remedies

1. **Transformations**:
   - Apply transformations like logarithmic, square root, or inverse to stabilize variance.
     - Example: Transform $y$ to $\log(y)$ if variability increases with $y$.
2. **Weighted Least Squares (WLS)**:
   - Assign weights to observations inversely proportional to their variance, giving less weight to observations with high variance.
3. **Robust Standard Errors**:
   - Use heteroscedasticity-consistent standard errors to correct inference issues without changing the model structure.
4. **Feature Engineering**:
   - Add omitted variables or modify predictors to capture missing patterns.

---

## Applications

1. **Econometrics**:
   - Commonly encountered when analyzing economic data like income, expenditure, or prices.
2. **Time Series Analysis**:
   - Variance may change over time due to structural shifts or trends.
3. **Predictive Modeling**:
   - Heteroscedasticity often arises in data with broad ranges or multiple subgroups.

---

## Example

Consider a regression model predicting household income:
- Residual plot shows a funnel-shaped pattern as predicted income increases.
- Apply a log transformation to income to stabilize variance:
  $$
  \log(y) = w_0 + w_1 x + \epsilon
  $$

---

## Related Topics

- [[Homoscedasticity]]: The assumption violated by heteroscedasticity.
- [[Ordinary Least Squares (OLS)]]: Relies on homoscedasticity for efficient estimates.
- [[Weighted Least Squares (WLS)]]: A solution for handling heteroscedasticity.
- [[Residual Analysis]]: Techniques for detecting variance issues.
- [[Breusch-Pagan Test]]: A statistical test for heteroscedasticity.

---

## Aliases
- Heteroscedasticity
- Non-Constant Variance

---

## Tags
#heteroscedasticity #regression #statistics #econometrics #timeseries

---

## Links to Explore
- [[Homoscedasticity]]: Understand the constant variance assumption.
- [[Ordinary Least Squares (OLS)]]: Learn how heteroscedasticity affects OLS models.
- [[Weighted Least Squares (WLS)]]: Discover a method to mitigate heteroscedasticity.
- [[Breusch-Pagan Test]]: Learn about detecting heteroscedasticity in regression models.
- [[Residual Analysis]]: Explore methods for analyzing and interpreting residuals.