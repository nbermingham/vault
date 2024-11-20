
## Overview
**Huber Loss** is a hybrid [[Loss Function]] commonly used in [[Machine Learning]] and [[Deep Learning]] for [[Regression]] tasks. It combines the advantages of [[Mean Squared Error]] and [[Mean Absolute Error (MAE)]], making it robust to outliers while remaining differentiable. The loss behaves like MSE for small errors and switches to MAE for larger errors to reduce the impact of outliers.

Huber Loss is ideal for scenarios where the data contains noise or outliers, but you still want smooth gradients for optimization.

---

## Formula
The Huber Loss is defined as:
$$
L_{\delta}(a) =
\begin{cases} 
\frac{1}{2}(y_i - \hat{y}_i)^2 & \text{if } |y_i - \hat{y}_i| \leq \delta \\
\delta \cdot |y_i - \hat{y}_i| - \frac{1}{2}\delta^2 & \text{if } |y_i - \hat{y}_i| > \delta
\end{cases}
$$
Where:
- $\delta$: Threshold parameter that determines the transition point between MSE and MAE.
- $y_i$: Actual target value for the $i$-th sample.
- $\hat{y}_i$: Predicted value for the $i$-th sample.

---

## Key Properties

1. **Smooth Transition**:
   - Acts as [[Mean Squared Error]] for errors smaller than $\delta$ and [[Mean Absolute Error (MAE)]] for larger errors.
2. **Differentiable Everywhere**:
   - Unlike MAE, Huber Loss is differentiable, making it easier to optimize with [[Gradient Descent]].

---

## Advantages

1. **Robustness to Outliers**:
   - Reduces the influence of outliers compared to [[Mean Squared Error]].
2. **Smooth Optimization**:
   - Provides smooth gradients for stable optimization, unlike the non-differentiable points in [[Mean Absolute Error (MAE)]].

---

## Disadvantages

1. **Hyperparameter Tuning**:
   - Requires tuning of the $\delta$ parameter, which may vary depending on the dataset.
2. **Computational Complexity**:
   - Slightly more complex to compute compared to simpler loss functions like MSE and MAE.

---

## Applications

1. **[[Regression]] Tasks**:
   - Used in models like [[Linear Regression]] and [[Neural Networks]] where robustness to outliers is essential.
2. **Time Series Forecasting**:
   - Effective for datasets with occasional anomalies.
3. **Robust Model Evaluation**:
   - Applied in evaluation when noise and outliers are present in the data.

---

## Comparison with Other Loss Functions

| Loss Function            | Sensitivity to Outliers | Differentiable | Best Used For                  |
|--------------------------|--------------------------|----------------|--------------------------------|
| [[Mean Squared Error]]   | High                    | Yes            | General regression tasks       |
| [[Mean Absolute Error]]  | Low                     | No (at zero)   | Robust regression tasks        |
| Huber Loss               | Medium                  | Yes            | Regression with outliers/noise |

---

## Related Topics

- [[Loss Function]]: Huber Loss is a robust alternative to standard loss functions.
- [[Mean Squared Error]]: Huber Loss transitions to MSE for small errors.
- [[Mean Absolute Error (MAE)]]: Huber Loss transitions to MAE for large errors.
- [[Gradient Descent]]: Huber Loss is optimized using gradient-based methods.
- [[Regression]]: A primary domain where Huber Loss is used effectively.

---

## Tags
#huber-loss #loss-function #regression #machinelearning #model-evaluation #robustness
