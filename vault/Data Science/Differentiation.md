## Overview
**Differentiation** is a fundamental concept in [[Calculus]] that measures how a function changes as its input changes. It computes the **derivative**, which represents the rate of change or slope of the function at any given point. Differentiation is widely used in [[Mathematics for Data Science|Mathematics]], [[Physics]], and [[Machine Learning]] for tasks such as optimization, motion analysis, and curve fitting.

---

## Key Concepts

### **1. Derivative**
The derivative of a function $f(x)$ at a point $x$ is defined as:
$$
f'(x) = \lim_{\Delta x \to 0} \frac{f(x + \Delta x) - f(x)}{\Delta x}
$$
Where:
- $f'(x)$: The derivative of $f(x)$.
- $\Delta x$: A small change in $x$.

### **2. Rules of Differentiation**
- **[[Power Rule]]**:
  $$
  \frac{d}{dx} \, x^n = n x^{n-1}
  $$
- **[[Sum Rule]]**:
  $$
  \frac{d}{dx} [f(x) + g(x)] = f'(x) + g'(x)
  $$
- **[[Product Rule]]**:
  $$
  \frac{d}{dx} [f(x) g(x)] = f'(x) g(x) + f(x) g'(x)
  $$
- **[[Quotient Rule]]**:
  $$
  \frac{d}{dx} \left[\frac{f(x)}{g(x)}\right] = \frac{f'(x) g(x) - f(x) g'(x)}{g(x)^2}
  $$
- **[[Chain Rule]]**:
  $$
  \frac{d}{dx} \, f(g(x)) = f'(g(x)) \cdot g'(x)
  $$

### **3. Higher-Order Derivatives**
- Second derivative:
  $$
  \frac{d^2 f}{dx^2}
  $$
  Measures the rate of change of the first derivative (e.g., acceleration in physics).

### **4. [[Partial Derivatives|partial differentiation]]**
- For multivariable functions, partial derivatives compute the rate of change with respect to one variable, holding others constant. Example:
  $$
  \frac{\partial f}{\partial x}
  $$

---

## Applications

1. **Optimization**:
   - Find local minima and maxima using derivatives (e.g., set $f'(x) = 0$ to locate critical points).
2. **Physics**:
   - Compute velocity and acceleration as the first and second derivatives of position.
3. **Machine Learning**:
   - Derivatives are key in [[Gradient Descent]] for minimizing loss functions.
4. **Economics**:
   - Analyze marginal cost and revenue using differentiation.
5. **Engineering**:
   - Model dynamic systems and compute rates of change in mechanical and electrical systems.

---

## Example
For the function:
$$
f(x) = x^3 - 2x^2 + 5x - 7
$$
The derivative is:
$$
f'(x) = 3x^2 - 4x + 5
$$

At $x = 2$:
$$
f'(2) = 3(2)^2 - 4(2) + 5 = 12 - 8 + 5 = 9
$$
This indicates the slope of $f(x)$ at $x = 2$ is $9$.

---

## Tools and Libraries

1. **Symbolic Computation**:
   - **SymPy**: Python library for symbolic differentiation.
   - Wolfram Alpha: Online tool for solving derivatives.
2. **Automatic Differentiation**:
   - [[TensorFlow]] and [[PyTorch]]: Automatically compute derivatives for optimization.
3. **Numerical Differentiation**:
   - **SciPy**: Compute derivatives numerically for complex functions.

---

## Related Topics

- [[Calculus]]: Differentiation is one of its core operations.
- [[Gradient Descent]]: Uses derivatives to optimize loss functions.
- [[Partial Derivatives]]: Extend differentiation to multivariable functions.
- [[Chain Rule]]: A fundamental rule for composite functions.
- [[Hessian Matrix]]: Second-order derivatives for curvature analysis.

---

## Aliases
- Differentiation
- Derivatives
- Differential Calculus

---

## Tags
#differentiation #calculus #mathematics #machinelearning #optimization #gradientdescent

---

## Links to Explore
- [[Gradient Descent]]: Learn how derivatives guide optimization.
- [[Partial Derivatives]]: Explore rates of change for multivariable functions.
- [[Chain Rule]]: Understand its importance in complex functions.
- [[Calculus]]: Discover its broader context in mathematics.
- [[Hessian Matrix]]: Analyze second-order effects in optimization.