---
aliases:
  - L2 Regularized Regression
  - L2 Regularization
---
## Overview

**Ridge Regression**, also known as **L2 Regularized Regression**, is an extension of [[Linear Regression]] that introduces a regularization term to reduce overfitting. It adds a penalty proportional to the square of the magnitude of the coefficients to the loss function, discouraging overly large coefficients and improving generalization.

Ridge Regression is particularly effective when the dataset contains multicollinearity (highly correlated features).

---

## Key Concepts

### Model Equation
Ridge Regression modifies the [[Linear Regression]] loss function by adding an $L2$ regularization term:
$$
\text{Loss} = \frac{1}{n} \sum_{i=1}^n (y_i - \hat{y}_i)^2 + \lambda \sum_{j=1}^p \beta_j^2
$$
Where:
- $y_i$: True values.
- $\hat{y}_i$: Predicted values.
- $\beta_j$: Model coefficients.
- $\lambda$: Regularization parameter (controls the strength of regularization).
- $p$: Number of features.

The regularization term $\lambda \sum_{j=1}^p \beta_j^2$ shrinks the coefficients toward zero, preventing overfitting.

### Regularization Parameter ($\lambda$)
- **Small $\lambda$**:
  - Minimal regularization, closer to [[Linear Regression]].
  - May result in [[Overfitting]].
- **Large $\lambda$**:
  - Strong regularization, shrinks coefficients more.
  - May lead to [[Underfitting]].

Selecting an optimal $\lambda$ is critical and is typically done using techniques like [[Cross-Validation]].

---

## Advantages

1. **Reduces Overfitting**:
   - Penalizes large coefficients, improving generalization on unseen data.
2. **Handles Multicollinearity**:
   - Stabilizes the solution when features are highly correlated.
3. **Works with Many Features**:
   - Suitable for high-dimensional datasets where $p \gg n$.

---

## Disadvantages

1. **Bias Introduction**:
   - Regularization introduces bias into the model.
2. **Interpretability**:
   - Coefficients are biased and harder to interpret compared to [[Linear Regression]].
3. **Not Suitable for Feature Selection**:
   - Unlike [[Lasso Regression]], Ridge Regression does not shrink coefficients to exactly zero.

---

## Applications

1. **High-Dimensional Data**:
   - Effective when the number of features is much larger than the number of observations (e.g., [[Genomics]] datasets).
2. **Multicollinear Features**:
   - Used in situations where features are highly correlated.
3. **Generalization Improvement**:
   - Improves the performance of models on unseen data by reducing variance.

---

## Variants

1. **Lasso Regression**:
   - Uses $L1$ regularization instead of $L2$, performing feature selection by shrinking some coefficients to zero.
2. **Elastic Net**:
   - Combines $L1$ and $L2$ regularization to balance feature selection and shrinkage.

---

## Example
Given a dataset:
| $x_1$ | $x_2$ | $y$  |
|-------|-------|------|
| 1     | 2     | 3    |
| 2     | 4     | 5    |
| 3     | 6     | 7    |

Without regularization:
- $\beta_1 = 10$, $\beta_2 = -10$

With Ridge Regression:
- For $\lambda = 0.1$, $\beta_1 = 5$, $\beta_2 = -5$

The regularization term penalizes large coefficients, resulting in smaller values for $\beta_1$ and $\beta_2$.

---

## Tools and Libraries

1. **Python Libraries**:
   - **Scikit-learn**: `Ridge` for Ridge Regression.
   - **Statsmodels**: Implements Ridge Regression through formula-based APIs.
2. **Hyperparameter Tuning**:
   - Use GridSearchCV or RandomizedSearchCV to find the optimal $\lambda$.

---

## Related Topics

- [[Linear Regression]]: Ridge Regression builds upon Linear Regression.
- [[Lasso Regression]]: An alternative that performs feature selection.
- [[Elastic Net]]: Combines the strengths of Ridge and [[Lasso Regression]].
- [[Regularization]]: Broader concept for preventing overfitting in machine learning models.
- [[Cross-Validation]]: Used for tuning the regularization parameter $\lambda$.

---

## Aliases
- Ridge Regression
- L2 Regularized Regression
- Tikhonov Regularization
- Shrinkage Regression

---

## Tags
#ridge-regression #regularization #machinelearning #linear-models #overfitting #datascience

---

## Links to Explore
- [[Linear Regression]]: Understand the base model that Ridge Regression builds upon.
- [[Lasso Regression]]: Compare Ridge to $L1$ regularization.
- [[Elastic Net]]: Explore the hybrid regularization technique.
- [[Regularization]]: Learn more about techniques to prevent overfitting.
- [[Cross-Validation]]: Discover how to tune $\lambda$ effectively.