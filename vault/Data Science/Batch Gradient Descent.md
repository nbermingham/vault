## Overview
**Batch Gradient Descent** is an optimization algorithm used in [[Machine Learning]] and [[Deep Learning]] to minimize a loss function by updating the model's parameters iteratively. It computes the gradient of the loss function with respect to all training examples (a full batch) before performing a single update to the model's parameters. 

Batch Gradient Descent is a foundational concept in training [[Neural Networks]] and other machine learning models.

---

## Key Concepts

### **1. How It Works**
- The algorithm iteratively updates the model parameters $\theta$ using the gradient of the loss function $J(\theta)$:
  $$
  \theta = \theta - \eta \nabla J(\theta)
  $$
  Where:
  - $\eta$: Learning rate, controlling the step size.
  - $\nabla J(\theta)$: Gradient of the loss function with respect to the parameters $\theta$.

- In **Batch Gradient Descent**, the gradient is calculated over the entire dataset:
  $$
  \nabla J(\theta) = \frac{1}{m} \sum_{i=1}^m \nabla J(\theta; x^{(i)}, y^{(i)})
  $$
  Where:
  - $m$: Number of training examples.
  - $(x^{(i)}, y^{(i)})$: Individual training examples and labels.

### **2. Full Batch Updates**
- The entire dataset is used to compute the gradient at each iteration.
- Parameters are updated only after processing all examples in the dataset.

---

## Advantages

1. **Deterministic Updates**:
   - Since the gradient is computed over the entire dataset, updates are consistent and converge smoothly.
2. **Stable Convergence**:
   - Less noisy compared to methods like [[Stochastic Gradient Descent (SGD)]].

---

## Disadvantages

1. **Computational Cost**:
   - Expensive for large datasets as it processes the entire dataset before each update.
2. **Memory Limitations**:
   - Requires the entire dataset to fit into memory, which may not be feasible for very large datasets.
3. **Slow Updates**:
   - Updates occur less frequently compared to [[Mini-Batch Gradient Descent]] and SGD.

---

## Applications

1. **Linear Models**:
   - Training algorithms like [[Linear Regression]] and [[Logistic Regression]].
2. **Deep Learning**:
   - Used in neural networks when dataset size is manageable.
3. **Convex Optimization**:
   - Solving convex problems where the deterministic gradient is preferred.

---

## Workflow

1. **Initialize Parameters**:
   - Start with random or zero-initialized parameters $\theta$.
2. **Compute Gradient**:
   - Calculate the gradient over the entire training dataset.
3. **Update Parameters**:
   - Apply the update rule $\theta = \theta - \eta \nabla J(\theta)$.
4. **Repeat**:
   - Iterate until convergence or a stopping criterion is met.

---

## Comparison with Other Gradient Descent Variants

| Feature                     | Batch Gradient Descent      | [[Stochastic Gradient Descent (SGD)]] | [[Mini-Batch Gradient Descent]]   |
|-----------------------------|-----------------------------|---------------------------------------|-----------------------------------|
| **Update Frequency**        | Once per epoch              | Once per example                     | Once per mini-batch              |
| **Stability**               | High                       | Low (noisy updates)                  | Moderate                         |
| **Speed**                   | Slow                       | Fast (frequent updates)              | Moderate                         |
| **Memory Efficiency**       | Low                        | High                                 | Moderate                         |

---

## Related Topics

- [[Stochastic Gradient Descent (SGD)]]: Updates parameters more frequently for faster but noisier convergence.
- [[Mini-Batch Gradient Descent]]: Combines the benefits of batch and stochastic methods.
- [[Loss Function]]: The objective function minimized by gradient descent.
- [[Learning Rate]]: A key hyperparameter that controls step size during updates.
- [[Optimization]]: The broader framework for improving model performance.

---

## Aliases
- Batch Gradient Descent
- Full-Batch Gradient Descent
- Deterministic Gradient Descent

---

## Tags
#gradientdescent #optimization #machinelearning #deeplearning #batchprocessing

---

## Links to Explore
- [[Stochastic Gradient Descent (SGD)]]: Compare with batch gradient descent for faster updates.
- [[Mini-Batch Gradient Descent]]: Learn about the hybrid method balancing stability and efficiency.
- [[Loss Function]]: Understand what gradient descent aims to minimize.
- [[Learning Rate]]: Explore its impact on optimization performance.
- [[Neural Networks]]: Discover how gradient descent powers their training.