## Overview
**Mini-Batch Gradient Descent** is an optimization technique used in [[Machine Learning]] and [[Deep Learning]] to update model parameters by computing gradients on small, random subsets (mini-batches) of the training dataset. It combines the benefits of both **[[Batch Gradient Descent]]** and **[[Stochastic Gradient Descent (SGD)]] (SGD)**, providing a balance between computational efficiency and convergence stability.

---

## Key Concepts

1. **Batch Size**:
   - The number of training examples in a mini-batch.
   - Common batch sizes: 32, 64, 128.
   - Larger batches require more memory but produce smoother updates.

2. **Parameter Update**:
   - For a mini-batch of size $m$, compute the gradient of the loss function $L$ with respect to parameters $\theta$:
   $$
   \theta = \theta - \eta \cdot \frac{1}{m} \sum_{i=1}^m \nabla_\theta L(x_i, y_i)
   $$
   Where:
   - $\eta$: Learning rate.
   - $(x_i, y_i)$: Training examples in the mini-batch.

---

## Advantages

1. **Efficient Computation**:
   - Mini-batches allow for parallelism on [[GPUs]], speeding up training.
2. **Convergence Stability**:
   - Reduces the noise in updates compared to [[Stochastic Gradient Descent]].
3. **Memory Efficiency**:
   - Requires less memory compared to [[Batch Gradient Descent]].

---

## Disadvantages

1. **Hyperparameter Sensitivity**:
   - Requires careful tuning of batch size and learning rate.
2. **Oscillations**:
   - Updates may oscillate or be less smooth than full-batch methods, especially with small batch sizes.

---

## Applications

1. **Deep Neural Networks**:
   - Commonly used in training [[Convolutional Neural Networks (CNNs)]] and [[Recurrent Neural Networks (RNNs)]].
2. **Large Datasets**:
   - Ideal for scenarios where full-batch gradient computation is computationally prohibitive.

---

## Related Topics

- [[Gradient Descent]]: Parent method of Mini-Batch Gradient Descent.
- [[Optimization]]: Broader field studying techniques for minimizing loss functions.
- [[Learning Rate Scheduling]]: Adjusting \( \eta \) during training to improve convergence.

---

## Tags
#gradient-descent #optimization #machinelearning #minibatch