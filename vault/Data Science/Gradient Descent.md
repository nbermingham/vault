## Overview
**Gradient Descent** is an optimization algorithm used to minimize a loss or cost function in machine learning models. By iteratively adjusting model parameters in the direction of the negative gradient, Gradient Descent seeks to find the minimum of the function. It is a foundational technique in [[Machine Learning]] and [[Deep Learning]].

---

## Key Concepts

### [[Objective Function]]
- The function $J(\theta)$ that Gradient Descent minimizes, often referred to as the **cost function** or **loss function**.
- Example: [[Mean Squared Error]] (MSE) in regression or [[Cross-Entropy Loss]] in [[Classification]].

### Gradient
- The gradient is the vector of [[Partial Derivatives]] of the objective function with respect to model parameters.
- It indicates the direction and rate of the steepest ascent. Gradient Descent moves in the opposite direction (steepest descent).

### Learning Rate $\alpha$
- A hyperparameter that controls the size of the steps taken during optimization.
  - **Small $\alpha$**: Converges slowly but more precisely.
  - **Large $\alpha$**: Converges faster but risks overshooting the minimum.

---

## Formula
For a parameter $\theta$, the update rule in Gradient Descent is:
$$
\theta = \theta - \alpha \frac{\partial J(\theta)}{\partial \theta}
$$
Where:
- $\alpha$: Learning rate.
- $\frac{\partial J(\theta)}{\partial \theta}$: Gradient of the cost function with respect to $\theta$.

---

## Types of Gradient Descent

### [[Batch Gradient Descent]]
- Computes the gradient using the entire dataset.
- **Advantages**:
  - Converges steadily.
  - Exact gradient computation.
- **Disadvantages**:
  - Computationally expensive for large datasets.
  - Requires large memory.

### [[Stochastic Gradient Descent (SGD)]]
- Updates parameters using the gradient computed from a single random sample.
- **Advantages**:
  - Faster updates.
  - Can escape local minima due to noise in updates.
- **Disadvantages**:
  - High variance in updates.
  - Converges less steadily compared to batch Gradient Descent.

### [[Mini-Batch Gradient Descent]]
- Uses a subset (mini-batch) of the dataset to compute the gradient at each step.
- **Advantages**:
  - Combines the efficiency of SGD with the stability of batch Gradient Descent.
  - Compatible with parallelization on GPUs.

---

## Variants of Gradient Descent

### [[Momentum]]
- Accelerates convergence by adding a momentum term to the updates.
$$
v = \beta v + \alpha \nabla J(\theta)
$$
$$
\theta = \theta - v
$$
- $v$: Velocity (exponentially weighted average of gradients).
- $\beta$: Momentum factor (e.g., 0.9).

### [[RMSProp]]
- Scales the learning rate by the moving average of the squared gradients.
$$
\theta = \theta - \frac{\alpha}{\sqrt{E[g^2] + \epsilon}} \nabla J(\theta)
$$
- Prevents oscillations in steep directions.

### [[Adam Optimizer]] (Adaptive Moment Estimation)
- Combines Momentum and RMSProp for faster and more adaptive learning.
- Maintains moving averages of both gradients and squared gradients.

### [[AdaGrad]]
- Adapts the learning rate for each parameter based on the historical sum of squared gradients.

---

## Applications
1. **Linear and Logistic Regression**:
   - Optimizes coefficients by minimizing the loss function.
2. [[Neural Networks]]:
   - Updates weights and biases in each layer to minimize loss during training.
3. **[[Clustering]]**:
   - Used in K-Means to update centroids iteratively.
4. **[[Recommender Systems]]**:
   - Optimizes latent factor representations in matrix factorization models.

---

## Challenges

1. **Choosing the Learning Rate**:
   - Too small: Slow convergence.
   - Too large: Divergence or oscillations.

2. **Local Minima and Saddle Points**:
   - Non-convex functions can trap the algorithm in local minima or saddle points.

3. **[[Exploding Gradients]] and [[Vanishing Gradients]]**:
   - Common in deep networks, especially during [[Backpropagation]] in [[Recurrent Neural Networks (RNNs)]].

4. **Convergence Issues**:
   - Requires proper initialization and potentially tuning learning rate schedules.

---

## Learning Rate Schedules
- **Constant Learning Rate**:
  - Fixed \( \alpha \) throughout training.
- **Decay Schedules**:
  - Reduce \( \alpha \) as training progresses:
    - Time-based decay: $\alpha_t = \frac{\alpha_0}{1 + kt}$
    - Step decay: Reduce $\alpha$ by a factor at specific intervals.
    - Exponential decay: $\alpha_t = \alpha_0 \cdot e^{-\lambda t}$

---

## Tools and Libraries
- **Python**:
  - TensorFlow: Optimizers like `tf.keras.optimizers.SGD`, `Adam`, `RMSProp`.
  - PyTorch: `torch.optim` module for built-in optimizers.
  - [[Scikit-learn]]: Implements optimization algorithms for regression and [[Classification]].
- **Visualization**:
  - TensorBoard: Tracks loss and gradient updates during training.

---

## Related Topics
- [[Optimization]]: Gradient Descent is one of many optimization algorithms.
- [[Stochastic Gradient Descent]]: Variant for faster updates.
- [[Adam Optimizer]]: Popular optimizer combining momentum and RMSProp.
- [[Learning Rate]]: Critical hyperparameter in Gradient Descent.

---

## Resources
- **Books**:
  - *Deep Learning* by Ian Goodfellow, Yoshua Bengio, and Aaron Courville.
  - *Pattern Recognition and Machine Learning* by Christopher Bishop.
- **Courses**:
  - Coursera: *Deep Learning Specialization* by Andrew Ng.
  - Udemy: *Machine Learning A-Z*.
- **Tutorials**:
  - TensorFlow and PyTorch documentation for Gradient Descent optimizers.
  - [[Scikit-learn]] guides for regression and [[Classification]].

---

## Tags
#gradientdescent #optimization #machinelearning #deep-learning #SGD