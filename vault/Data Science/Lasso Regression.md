---
aliases:
  - L1 Regularization
  - Sparse Regression
---
## Overview
**Lasso Regression** (Least Absolute Shrinkage and Selection Operator) is a type of [[Linear Regression]] that incorporates **L1 Regularization**. It adds a penalty term to the loss function proportional to the absolute sum of the model's coefficients, encouraging sparsity by driving some coefficients to exactly zero. This makes Lasso particularly useful for feature selection and improving model interpretability.

---

## Formula

The objective function for Lasso Regression is:
$$
L = \frac{1}{N} \sum_{i=1}^N \left( y_i - \hat{y}_i \right)^2 + \lambda \sum_{j=1}^p |w_j|
$$
Where:
- $N$: Number of samples.
- $p$: Number of features.
- $y_i$: True value for the $i$-th sample.
- $\hat{y}_i$: Predicted value for the $i$-th sample.
- $w_j$: Coefficient for the $j$-th feature.
- $\lambda$: Regularization strength.

---

## Key Characteristics

1. **Feature Selection**:
   - Lasso shrinks less important feature coefficients to exactly zero, effectively performing feature selection.
2. **Sparse Models**:
   - Lasso models are often sparse, meaning they include only the most relevant features.
3. **Sensitivity to Correlated Features**:
   - Lasso tends to select one feature from a group of highly correlated features and ignore the others.

---

## Applications

1. **Feature Selection**:
   - Automatically eliminates irrelevant or redundant features by assigning zero weights.
2. **High-Dimensional Data**:
   - Useful for datasets where the number of features exceeds the number of samples (e.g., genomics, text data).
3. **Prediction Models**:
   - Builds interpretable models by focusing on a smaller set of features.

---

## Advantages

1. **Feature Selection**:
   - Automatically excludes irrelevant features, simplifying the model.
2. **Improves Interpretability**:
   - Sparse solutions make it easier to understand the relationship between features and the target.
3. **Handles High-Dimensional Data**:
   - Effective in cases where the number of features is much larger than the number of samples.

---

## Disadvantages

1. **Bias in Coefficients**:
   - Lasso may overly shrink coefficients, introducing bias in predictions.
2. **Handles Correlated Features Poorly**:
   - May arbitrarily select one feature from a group of correlated features.
3. **Non-Differentiability**:
   - The $L1$ penalty is not differentiable at zero, requiring specialized solvers.

---

## Key Differences from [[Ridge Regression]]

| Feature                     | Lasso Regression           | [[Ridge Regression]]          |
|-----------------------------|----------------------------|--------------------------------|
| **Penalty**                 | L1 Regularization          | L2 Regularization             |
| **Feature Selection**       | Performs feature selection | Does not perform feature selection |
| **Sparsity**                | Produces sparse models     | Produces non-sparse models    |
| **Correlated Features**     | Arbitrarily selects one    | Distributes weights among all |

---

## Implementation in Practice

1. **Hyperparameter Tuning**:
   - $\lambda$ controls the strength of regularization:
     - Large $\lambda$: Stronger penalty, more coefficients set to zero.
     - Small $\lambda$: Weaker penalty, less sparsity.

2. **Tools**:
   - **Python Libraries**:
     - [[Scikit-learn]]: Provides `Lasso` and `LassoCV` for cross-validated Lasso.
     - [[Statsmodels]]: Allows for detailed statistical summaries.

---

## Related Topics

- [[Linear Regression]]: The base model upon which Lasso builds.
- [[Ridge Regression]]: Uses L2 regularization instead of L1.
- [[Elastic Net]]: Combines L1 and L2 regularization.
- [[Regularization]]: General framework for controlling model complexity.
- [[Feature Selection]]: A key application of Lasso Regression.

---

## Aliases
- Lasso Regression
- L1 Regularized Regression
- Sparse Regression

---

## Tags
#lassoregression #linearregression #featureselection #machinelearning #regularization

---

## Links to Explore
- [[Linear Regression]]: Understand the base model used in Lasso.
- [[Ridge Regression]]: Compare Lasso with its L2 counterpart.
- [[Elastic Net]]: Explore a hybrid of L1 and L2 regularization.
- [[Regularization]]: Learn about controlling overfitting through penalties.
- [[Feature Selection]]: Discover how Lasso automates this process.
