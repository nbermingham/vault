## Overview
**R-Squared** (denoted as $R^2$), also known as the **Coefficient of Determination**, is a statistical metric used in [[Regression]] analysis to evaluate the goodness-of-fit of a model. It measures the proportion of variance in the target variable ($y$) that is explained by the input features ($x$). 

R-Squared values range from 0 to 1, where:
- $R^2 = 1$: Perfect fit; the model explains all the variance in $y$.
- $R^2 = 0$: The model does not explain any of the variance in $y$.

---

## Formula
The formula for $R^2$ is:
$$
R^2 = 1 - \frac{\text{SS}_{\text{res}}}{\text{SS}_{\text{tot}}}
$$
Where:
- $\text{SS}_{\text{res}}$ (Residual Sum of Squares): Sum of squared differences between actual and predicted values.
  $$
  \text{SS}_{\text{res}} = \sum_{i=1}^n (y_i - \hat{y}_i)^2
  $$
- $\text{SS}_{\text{tot}}$ (Total Sum of Squares): Sum of squared differences between actual values and the mean of $y$.
  $$
  \text{SS}_{\text{tot}} = \sum_{i=1}^n (y_i - \bar{y})^2
  $$
- $y_i$: Actual value of the target variable.
- $\hat{y}_i$: Predicted value from the model.
- $\bar{y}$: Mean of the actual values.

---

## Interpretation
1. **High $R^2$**:
   - Indicates that the model explains a large proportion of the variance in the target variable.
2. **Low $R^2$**:
   - Indicates that the model explains little of the variance, suggesting it may not capture the underlying patterns effectively.

---

## Limitations
1. **Does Not Indicate Causation**:
   - A high $R^2$ does not imply that the input features cause changes in the target variable.
2. **Sensitive to Overfitting**:
   - Adding more features can artificially inflate $R^2$ even if those features are irrelevant.
3. **Not Always Suitable for Non-Linear Models**:
   - For non-linear relationships, $R^2$ may not fully capture model performance.

---

## Adjusted R-Squared
To address the inflation of $R^2$ with additional features, the **Adjusted R-Squared** is used:
$$
R_{\text{adj}}^2 = 1 - \frac{\text{SS}_{\text{res}} / (n - k - 1)}{\text{SS}_{\text{tot}} / (n - 1)}
$$
Where:
- $n$: Number of data points.
- $k$: Number of independent variables (features).

Adjusted $R^2$ penalizes models for including irrelevant features, providing a more accurate assessment of model performance.

---

## Applications

1. **Model Evaluation**:
   - Used to determine how well a regression model fits the data.
2. **Feature Selection**:
   - Helps assess the contribution of individual features to the model's explanatory power.
3. **Comparison of Models**:
   - Compare different regression models to identify the best fit.

---

## Example
Consider a dataset where:
- $y$ (actual values): [3, 5, 7, 9]
- $\hat{y}$ (predicted values): [2.8, 5.1, 6.9, 9.2]

1. **Mean of $y$**:
   $$
   \bar{y} = \frac{3 + 5 + 7 + 9}{4} = 6
   $$
2. **SS$_{\text{tot}}$**:
   $$
   \text{SS}_{\text{tot}} = (3 - 6)^2 + (5 - 6)^2 + (7 - 6)^2 + (9 - 6)^2 = 18
   $$
3. **SS$_{\text{res}}$**:
   $$
   \text{SS}_{\text{res}} = (3 - 2.8)^2 + (5 - 5.1)^2 + (7 - 6.9)^2 + (9 - 9.2)^2 = 0.14
   $$
4. **R-Squared**:
   $$
   R^2 = 1 - \frac{\text{SS}_{\text{res}}}{\text{SS}_{\text{tot}}} = 1 - \frac{0.14}{18} \approx 0.992
   $$

---

## Related Topics

- [[Mean Squared Error]]: Another metric for evaluating regression models.
- [[Adjusted R-Squared]]: Penalizes for adding irrelevant features.
- [[Linear Regression]]: The most common use case for $R^2$.
- [[Overfitting]]: A model with artificially high $R^2$ may be overfitting.
- [[Feature Selection]]: High $R^2$ can guide feature importance evaluation.

---

## Aliases
- R-Squared
- Coefficient of Determination
- $R^2$

---

## Tags
#r-squared #regression #model-evaluation #datascience #machinelearning

---

## Links to Explore
- [[Mean Squared Error]]: Compare with $R^2$ for regression evaluation.
- [[Adjusted R-Squared]]: Learn how it improves on standard $R^2$.
- [[Linear Regression]]: The primary model where $R^2$ is used.
- [[Feature Selection]]: Explore the impact of features on $R^2$.