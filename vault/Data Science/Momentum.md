## Overview
**Momentum** is an optimization technique used in [[Machine Learning]] and [[Deep Learning]] to accelerate the convergence of [[Gradient Descent]] algorithms, particularly in the presence of high-curvature, [[saddle points]], or [[noisy gradients]]. By incorporating a moving average of past gradients, Momentum smooths updates and helps the optimizer navigate toward the minimum more effectively.

---

## Key Concepts

### **1. How Momentum Works**

Momentum introduces a velocity term to update the model’s parameters, adding inertia to the optimization process. This helps the optimizer build speed in consistent gradient directions while damping oscillations in directions with fluctuating gradients.

The parameter update rule with momentum is:
$$
v_t = \beta v_{t-1} + (1 - \beta) \nabla J(\theta)
$$
$$
\theta_t = \theta_{t-1} - \eta v_t
$$
Where:
- $\theta_t$: Model parameters at iteration $t$.
- $\eta$: Learning rate.
- $v_t$: Velocity term at iteration $t$.
- $\beta$: Momentum coefficient, typically between 0.8 and 0.99.
- $\nabla J(\theta)$: Gradient of the loss function.

---

## Features

1. **Velocity Term**:
   - Maintains a running average of past gradients to accelerate convergence in consistent directions.
2. **Reduces Oscillations**:
   - Stabilizes updates, particularly in steep, narrow valleys or noisy gradient regions.
3. **Hyperparameter**:
   - The momentum coefficient $\beta$ controls the influence of past gradients. Larger values increase smoothing.

---

## Applications

1. **Deep Learning**:
   - Commonly used in training [[Neural Networks]], especially for complex architectures like [[Convolutional Neural Networks (CNNs)]] and [[Recurrent Neural Networks (RNNs)]].
2. **Non-Convex Optimization**:
   - Effective in navigating the non-convex landscapes of deep learning loss functions.
3. **Accelerated Convergence**:
   - Particularly useful for problems with high-curvature or noisy gradients.

---

## Advantages

1. **Faster Convergence**:
   - Builds momentum in consistent directions, speeding up convergence in convex regions.
2. **Smooth Updates**:
   - Reduces noisy oscillations in directions with varying gradients.
3. **Simple to Implement**:
   - Easily added to standard gradient descent algorithms.

---

## Disadvantages

1. **Hyperparameter Sensitivity**:
   - Performance depends on choosing an appropriate value for $\beta$.
2. **Overshooting**:
   - In some cases, momentum may cause the optimizer to overshoot the minimum.

---

## Workflow

1. **Initialize Parameters**:
   - Start with randomly initialized weights $\theta$ and velocity $v = 0$.
2. **Compute Gradient**:
   - Calculate $\nabla J(\theta)$ for the current parameters.
3. **Update Velocity**:
   - Compute $v_t$ using the momentum equation.
4. **Update Parameters**:
   - Adjust $\theta$ using the velocity term.
5. **Repeat**:
   - Iterate until convergence or a stopping criterion is met.

---

## Related Topics

- [[Gradient Descent]]: Momentum is an enhancement to standard gradient descent.
- [[Stochastic Gradient Descent (SGD)]]: Combines well with momentum for stochastic updates.
- [[Adam Optimizer]]: Incorporates momentum with adaptive learning rates.
- [[Optimization]]: Momentum is a key technique in the broader field of optimization.

---

## Aliases
- Momentum
- Momentum-Based Optimization
- Velocity Term

---

## Tags
#momentum #gradientdescent #optimization #machinelearning #deeplearning #neuralnetworks

---

## Links to Explore
- [[Gradient Descent]]: Learn about the foundational optimization algorithm enhanced by momentum.
- [[Stochastic Gradient Descent (SGD)]]: Explore how momentum complements stochastic updates.
- [[Adam Optimizer]]: Discover how Adam integrates momentum into its framework.
- [[Optimization]]: Understand the broader context of momentum in optimization.
- [[Neural Networks]]: See how momentum accelerates deep learning training.