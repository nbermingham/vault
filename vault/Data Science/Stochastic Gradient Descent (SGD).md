## Overview

**Stochastic Gradient Descent (SGD)** is an optimization algorithm used in [[Machine Learning]] and [[Deep Learning]] for minimizing loss functions by updating model parameters using the gradient of the loss computed for a single randomly selected training example at each step.

Unlike [[Batch Gradient Descent]], which computes gradients over the entire dataset, SGD updates parameters more frequently, leading to faster but noisier convergence.

---

## Key Formula
For a training example $(x_i, y_i)$:
$$
\theta = \theta - \eta \cdot \nabla_\theta L(x_i, y_i)
$$
Where:
- $\theta$: Model parameters.
- $\eta$: Learning rate.
- $\nabla_\theta L(x_i, y_i)$: Gradient of the loss $ L $ for the training example $(x_i, y_i)$.

---

## Advantages

1. **Faster Updates**:
   - Performs updates after each sample, making it computationally efficient for large datasets.
2. **Exploration of Loss Surface**:
   - Noisy updates help escape local minima and saddle points.

---

## Disadvantages

1. **Noisy Convergence**:
   - High variance in updates can lead to instability and slower convergence to the global minimum.
2. **Sensitivity to Learning Rate**:
   - Requires careful tuning of the learning rate $\eta$.

---

## Applications

1. **Training Neural Networks**:
   - Often used with modifications (e.g., [[Mini-Batch Gradient Descent]] or momentum-based optimizers).
2. **Large Datasets**:
   - Effective when full-batch gradient computation is computationally expensive.

---

## Variants
1. **Mini-Batch Gradient Descent**:
   - Combines benefits of SGD and Batch Gradient Descent.
2. **Momentum**:
   - Adds an exponentially weighted average of past gradients to the update for smoother convergence.
3. **Adaptive Methods**:
   - Algorithms like [[Adam Optimizer]] build on SGD with adaptive learning rates.

---

## Related Topics

- [[Gradient Descent]]: Parent method of SGD.
- [[Optimization]]: Field of study encompassing gradient-based methods.
- [[Loss Function]]: Function minimized during training.

---

## Tags
#gradient-descent #optimization #machinelearning #SGD