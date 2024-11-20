## Overview

**Mean Absolute Error (MAE)** is a commonly used [[Loss Function]] in [[Machine Learning]] and [[Deep Learning]], especially for [[Regression]] tasks. It calculates the average of the absolute differences between predicted values and actual target values. Unlike [[Mean Squared Error]], MAE is less sensitive to outliers because it does not square the errors.

MAE provides an interpretable metric in the same units as the target variable, making it easier to understand and apply in practical scenarios.

---

## Formula
The formula for MAE is:
$$
MAE = \frac{1}{n} \sum_{i=1}^n |y_i - \hat{y}_i|
$$
Where:
- $n$: Number of samples.
- $y_i$: Actual target value for the $i$-th sample.
- $\hat{y}_i$: Predicted value for the $i$-th sample.

---

## Key Properties

1. **Robust to Outliers**:
   - MAE penalizes errors linearly, making it more robust to extreme values compared to [[Mean Squared Error]].
2. **Non-Differentiable**:
   - MAE is not differentiable at $y_i = \hat{y}_i$, but approximations like [[Huber Loss]] address this issue.

---

## Advantages

1. **Interpretability**:
   - Errors are measured in the same units as the target variable, making MAE intuitive to interpret.
2. **Outlier Robustness**:
   - Less sensitive to extreme deviations compared to [[Mean Squared Error]].

---

## Disadvantages

1. **Optimization Challenges**:
   - Non-differentiability at zero can make it harder to optimize using [[Gradient Descent]].
2. **Equal Weighting**:
   - Treats all errors equally, which may not be desirable in some applications (e.g., emphasizing larger errors).

---

## Applications

1. **[[Regression]] Tasks**:
   - Used in [[Linear Regression]], [[Decision Trees]], and [[Neural Networks]] when robustness to outliers is a priority.
2. **Forecasting**:
   - Commonly applied in time series forecasting tasks.
3. **[[Model Evaluation]]**:
   - Serves as an evaluation metric for regression models when interpretability is required.

---

## Variants

1. **[[Mean Squared Error]]**:
   - Squared errors penalize larger deviations more heavily.
2. **Huber Loss**:
   - Combines the robustness of MAE with the differentiability of MSE.
3. **Log-Cosh Loss**:
   - Similar to MAE but differentiable everywhere, making it smoother for optimization.

---

## Related Topics

- [[Loss Function]]: MAE is a foundational metric for regression tasks.
- [[Mean Squared Error]]: A commonly used alternative to MAE.
- [[Huber Loss]]: A hybrid loss function that blends the properties of MSE and MAE.
- [[Gradient Descent]]: Optimization techniques for minimizing MAE during model training.
- [[Model Evaluation]]: MAE is often used to compare regression model performance.

---

## Tags
#mean-absolute-error #loss-function #regression #machinelearning #model-evaluation