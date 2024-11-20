## Overview
**Calculus** is a branch of mathematics focused on studying rates of change ([[Differentiation]]) and accumulation ([[Integration]]). It is essential in fields like physics, engineering, economics, and [[Machine Learning]], forming the foundation of optimization, modeling, and analysis of dynamic systems.

---

## Key Concepts

### **1. [[Differentiation]]**
- Differentiation measures the rate of change of a function with respect to its variables.
- **Derivative**: The instantaneous rate of change of a function $f(x)$ is:
  $$
  f'(x) = \lim_{\Delta x \to 0} \frac{f(x + \Delta x) - f(x)}{\Delta x}
  $$
- **Applications**:
  - Compute slopes of curves.
  - Optimize functions using [[Gradient Descent]].
  - Solve equations in [[Physics]] (e.g., velocity, acceleration).

### **2. Partial Derivatives**
- Extends differentiation to multivariable functions.
- Example: $\frac{\partial f}{\partial x}$ measures how $f$ changes with $x$, keeping other variables constant.
- Widely used in [[Machine Learning]] for calculating gradients and optimizing loss functions.

### **3. Integration**
- Integration measures the accumulation of quantities (area under curves).
- **Definite Integral**: Computes the area under a curve between $a$ and $b$:
  $$
  \int_a^b f(x) \, dx
  $$
- **Indefinite Integral**: Represents the antiderivative:
  $$
  \int f(x) \, dx = F(x) + C
  $$
- **Applications**:
  - Compute areas, volumes, and probabilities.
  - Solve differential equations.
  - Model systems in [[Economics]] and [[Physics]].

### **4. Fundamental Theorem of Calculus**
Links differentiation and integration:
$$
\int_a^b f'(x) \, dx = f(b) - f(a)
$$

---

## Applications

1. **Optimization**:
   - Use derivatives to find minima and maxima in functions (e.g., loss minimization in [[Machine Learning]]).
2. **Modeling**:
   - Analyze rates of change in dynamic systems like fluid flow or population growth.
3. **Probability and Statistics**:
   - Integration is used to compute probabilities and expectations in [[Probability Distributions]].
4. **Physics and Engineering**:
   - Solve problems involving motion, energy, and systems of differential equations.

---

## Tools and Libraries

1. **Symbolic Computation**:
   - **SymPy**: Python library for symbolic calculus.
   - Wolfram Alpha: Online tool for solving calculus problems.
2. **Numerical Methods**:
   - **SciPy**: Python library for numerical integration.
   - **MATLAB**: Widely used for both symbolic and numerical calculus.
3. **Deep Learning Frameworks**:
   - [[TensorFlow]] and [[PyTorch]]: Use calculus for automatic differentiation and optimization.

---

## Related Topics

- [[Partial Derivatives]]: Analyze rates of change in multivariable functions.
- [[Gradient Descent]]: Uses derivatives to minimize loss functions.
- [[Hessian Matrix]]: Second-order derivatives for curvature analysis.
- [[Optimization]]: Framework for finding minima and maxima.
- [[Probability Distributions]]: Involves integration to compute cumulative probabilities.

---

## Aliases
- Calculus
- Mathematical Calculus
- Differentiation and Integration

---

## Tags
#calculus #mathematics #machinelearning #optimization #differentiation #integration

---

## Links to Explore
- [[Partial Derivatives]]: Understand their role in multivariable functions.
- [[Gradient Descent]]: Learn how derivatives guide optimization.
- [[Integration]]: Explore applications of accumulation in modeling.
- [[Optimization]]: Dive into finding extrema using calculus.
- [[Hessian Matrix]]: Analyze second-order effects using calculus.