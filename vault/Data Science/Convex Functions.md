## Overview
A **Convex Function** is a type of mathematical function where a line segment between any two points on the graph of the function lies above or on the graph. Convex functions are fundamental in [[Optimization]] because they guarantee that any local minimum is also a global minimum, simplifying optimization tasks.

Convex functions are widely used in [[Machine Learning]], [[Economics]], and mathematical modeling due to their desirable properties for optimization algorithms like [[Gradient Descent]].

---

## Mathematical Definition

A function $f: \mathbb{R}^n \to \mathbb{R}$ is convex if:
$$
f(\lambda x_1 + (1-\lambda)x_2) \leq \lambda f(x_1) + (1-\lambda)f(x_2), \quad \forall x_1, x_2 \in \mathbb{R}^n, \; \lambda \in [0, 1]
$$
Where:
- $x_1, x_2$: Points in the domain of $f$.
- $\lambda$: A scalar weight between 0 and 1.

---

## Key Properties

1. **First Derivative (1D Case)**:
   - A differentiable function $f(x)$ is convex if:
     $$
     f'(x_2) \geq f'(x_1), \quad \forall x_2 > x_1
     $$

2. **Second Derivative (1D Case)**:
   - A twice-differentiable function $f(x)$ is convex if:
     $$
     f''(x) \geq 0, \quad \forall x \in \text{domain of } f
     $$

3. **Hessian Matrix (Multivariate Case)**:
   - A twice-differentiable function $f(x)$ is convex if its [[Hessian Matrix]] is positive semi-definite:
     $$
     H(f(x)) \succeq 0
     $$

---

## Examples

1. **Linear Functions**:
   - Any linear function $f(x) = ax + b$ is convex.
2. **Quadratic Functions**:
   - $f(x) = ax^2 + bx + c$ is convex if $a > 0$.
3. **Logarithmic Functions**:
   - $f(x) = -\log(x)$ is convex for $x > 0$.
4. **Exponential Functions**:
   - $f(x) = e^x$ is convex over all $x$.

---

## Applications

1. **Optimization**:
   - Convex functions simplify [[Optimization]] problems because any local minimum is also a global minimum.
   - Algorithms like [[Gradient Descent]] perform well on convex functions.
2. **Machine Learning**:
   - Loss functions like [[Log-Loss Function]], [[Mean Squared Error]], and [[Hinge Loss]] are convex, enabling efficient training of models like [[Logistic Regression]] and [[Support Vector Machines (SVMs)]].
3. **Economics**:
   - Utility functions and cost minimization problems are often modeled as convex functions.

---

## Advantages

1. **Global Optimality**:
   - Convex functions ensure that any local minimum is the global minimum.
2. **Computational Simplicity**:
   - Efficient optimization methods exist for convex functions.
3. **Theoretical Guarantees**:
   - Convexity allows for strong guarantees on convergence and solution quality.

---

## Disadvantages

1. **Limited Expressiveness**:
   - Many real-world problems involve non-convex functions, requiring more complex optimization methods.
2. **Restricted Assumptions**:
   - The assumption of convexity may not hold for highly non-linear or multimodal functions.

---

## Related Topics

- [[Optimization]]: Convex functions simplify optimization tasks.
- [[Gradient Descent]]: Performs efficiently on convex loss functions.
- [[Hessian Matrix]]: Used to determine convexity in multivariate functions.
- [[Loss Function]]: Many commonly used loss functions in machine learning are convex.
- [[Non-Convex Functions]]: Compare with functions that pose greater optimization challenges.

---

## Aliases
- Convex Functions
- Convexity
- Convex Optimization Functions

---

## Tags
#convexfunctions #optimization #mathematics #machinelearning #gradientdescent

---

## Links to Explore
- [[Optimization]]: Learn about solving convex and non-convex problems.
- [[Gradient Descent]]: Discover how convexity guarantees convergence.
- [[Hessian Matrix]]: Explore how it determines convexity in multivariate functions.
- [[Log-Loss Function]]: A convex loss function used in classification tasks.
- [[Non-Convex Functions]]: Understand challenges posed by non-convex problems.