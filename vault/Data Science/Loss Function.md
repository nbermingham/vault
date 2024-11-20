# Loss Function

## Overview
A **Loss Function** is a mathematical function used in [[Machine Learning]] and [[Deep Learning]] to quantify the difference between the predicted output of a model and the actual target values. It guides the optimization process by providing a metric to minimize during training.

Loss functions are central to tasks like regression, classification, and reinforcement learning, as they define the learning objective.

---

## Key Concepts

1. **Minimization**:
   - The goal of training is to minimize the loss function by updating model parameters using optimization algorithms like [[Gradient Descent]].

2. **Types of Loss Functions**:
   - Regression Losses (e.g., [[Mean Squared Error]]).
   - Classification Losses (e.g., [[Cross-Entropy Loss]]).
   - Custom Losses (e.g., domain-specific objectives).

---

## Common Loss Functions

### 1. **Mean Squared Error (MSE)**
Used for regression tasks:
$$
L = \frac{1}{n} \sum_{i=1}^n (y_i - \hat{y}_i)^2
$$
Where:
- $n$: Number of samples.
- $y_i$: Actual value.
- $\hat{y}_i$: Predicted value.

### 2. **Cross-Entropy Loss**
Used for classification tasks:
$$
L = -\sum_{i=1}^C y_i \log(\hat{y}_i)
$$
Where:
- $C$: Number of classes.
- $y_i$: One-hot encoded true label.
- $\hat{y}_i$: Predicted probability for class $i$.

### 3. **[[Hinge Loss]]**
Used for binary classification with [[support vector machines]]:
$$
L = \frac{1}{n} \sum_{i=1}^n \max(0, 1 - y_i \cdot \hat{y}_i)
$$
Where:
- $y_i$: True label ($+1$ or $-1$).
- $\hat{y}_i$: Predicted output.

---

## Applications

1. **[[Regression]]**:
   - Models like Linear Regression and Neural Networks use MSE or MAE ([[Mean Absolute Error]]).
2. **[[Classification]]**:
   - Models like [[Logistic Regression]] and [[Neural Networks]] use Cross-Entropy Loss.
3. **[[Reinforcement Learning]]**:
   - Uses custom reward-based loss functions.

---

## Choosing the Right Loss Function

1. **Task-Specific**:
   - The choice of loss function depends on whether the task is regression, classification, or another specialized application.
2. **Robustness**:
   - Loss functions like Huber Loss are robust to outliers compared to MSE.

---

## Related Topics

- [[Optimization]]: Loss functions are minimized during the training process.
- [[Gradient Descent]]: Computes gradients of the loss to update parameters.
- [[Regularization]]: Adds penalty terms to the loss function to reduce overfitting.

---

## Tags
#loss-function #optimization #machinelearning #deeplearning