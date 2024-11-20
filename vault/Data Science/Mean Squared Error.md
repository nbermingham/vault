## Overview
**Mean Squared Error (MSE)** is a common loss function used in [[Machine Learning]] and [[Deep Learning]], particularly for [[Regression]] tasks. It measures the average squared difference between the predicted values and the actual target values, penalizing larger errors more heavily than smaller ones.

MSE is widely used due to its simplicity and sensitivity to significant deviations in predictions. It is also a standard metric for [[Model Evaluation]] in regression tasks.

---

## Formula
The formula for MSE is:
$$
MSE = \frac{1}{n} \sum_{i=1}^n (y_i - \hat{y}_i)^2
$$
Where:
- $n$: Number of samples.
- $y_i$: Actual target value for the $i$-th sample.
- $\hat{y}_i$: Predicted value for the $i$-th sample.

---

## Key Properties

1. **Penalizes Large Errors**:
   - Squaring the error amplifies the impact of larger deviations, making MSE sensitive to outliers.
2. **[[Convex Function]]**:
   - MSE is convex with respect to the model parameters, making it easier to optimize using gradient-based methods.
3. **Differentiable**:
   - MSE is differentiable, which is essential for optimization algorithms like [[Gradient Descent]].

---

## Advantages

1. **Simplicity**:
   - Easy to compute and implement.
2. **Smooth Gradients**:
   - Facilitates stable optimization during training.

---

## Disadvantages

1. **Sensitivity to Outliers**:
   - Outliers disproportionately affect the loss due to squaring errors.
2. **Not Robust to Scale**:
   - The magnitude of MSE depends on the scale of the target variable, requiring normalization or standardization in some cases.

---

## Applications

1. **[[Regression]] Tasks**:
   - Models like [[Linear Regression]], [[Decision Trees]], and [[Neural Networks]] use MSE to minimize prediction errors.
2. **Forecasting**:
   - Commonly used in time series prediction and other forecasting tasks.
3. **[[Model Evaluation]]**:
   - Used as a metric to evaluate regression model performance.

---

## Variants

1. **[[Mean Absolute Error (MAE)]]**:
   - Uses absolute differences instead of squared differences for robustness to outliers.
   $$ MAE = \frac{1}{n} \sum_{i=1}^n |y_i - \hat{y}_i| $$

2. **[[Huber Loss]]**:
   - Combines the strengths of MSE and MAE, making it robust to outliers while retaining differentiability.

---

## Related Topics

- [[Loss Function]]: MSE is a standard loss function for regression tasks.
- [[Gradient Descent]]: Used to minimize MSE during model training.
- [[Linear Regression]]: A common model where MSE is used as the objective function.
- [[Mean Absolute Error (MAE)]]: An alternative loss function less sensitive to outliers.

---

## Tags
#mean-squared-error #loss-function #regression #machinelearning #model-evaluation