---
aliases:
  - CDF
  - Cumulative Distribution Function
---
## Overview

A **Cumulative Distribution Function (CDF)** represents the probability that a random variable $X$ takes on a value less than or equal to $x$. It provides a cumulative measure of probability and is fundamental in both [[Probability]] and [[Statistics]]. The CDF applies to both [[Discrete Distributions]] and [[Continuous Distributions]].

Mathematically, the CDF is defined as:
$$
F(x) = P(X \leq x)
$$
Where:
- $F(x)$: Cumulative probability up to $x$.
- $X$: The random variable.
- $x$: A specific value of $X$.

---

## Properties

1. **Range**:
   - $F(x) \in [0, 1]$ for all $x$.
2. **[[Monotonicity]]**:
   - $F(x)$ is a non-decreasing function.
3. **Limits**:
   - $\lim_{x \to -\infty} F(x) = 0$ and $\lim_{x \to \infty} F(x) = 1$.
4. **Discrete Case**:
   - For a discrete random variable:
     $$
     F(x) = \sum_{x_i \leq x} P(X = x_i)
     $$
5. **Continuous Case**:
   - For a continuous random variable, the CDF is the integral of the [[Probability Density Function (PDF)]]:
     $$
     F(x) = \int_{-\infty}^x f(t) \, dt
     $$

---

## Applications

1. **Statistical Analysis**:
   - Analyze and visualize cumulative probabilities in datasets.
2. **Quantile Calculation**:
   - Find the value of $x$ corresponding to a specific cumulative probability (inverse CDF).
3. **Hypothesis Testing**:
   - Used in computing $p$-values for statistical tests.
4. **Simulation**:
   - Generate random samples from specific distributions using the CDF.

---

## Example

### Discrete Example (Rolling a Die)
Let $X$ represent the outcome of rolling a fair six-sided die. The PMF is:
$$
P(X = x) = \frac{1}{6}, \, x \in \{1, 2, 3, 4, 5, 6\}
$$
The CDF is:
- $F(1) = P(X \leq 1) = \frac{1}{6}$
- $F(2) = P(X \leq 2) = \frac{2}{6}$
- $F(3) = P(X \leq 3) = \frac{3}{6}$, and so on.

### Continuous Example (Exponential Distribution)
For an Exponential Distribution with rate parameter $\lambda = 2$, the CDF is:
$$
F(x) = 1 - e^{-2x}, \, x \geq 0
$$
If $x = 1$:
$$
F(1) = 1 - e^{-2 \cdot 1} = 1 - e^{-2} \approx 0.8647
$$

---

## Related Topics

- [[Probability Distributions]]: Frameworks for describing random variables using CDFs.
- [[Probability Density Function (PDF)]]: The derivative of the CDF for continuous variables.
- [[Probability Mass Function (PMF)]]: Summarizes probabilities for discrete variables.
- [[Quantiles]]: Find cutoffs in a distribution using the CDF.

---

## Aliases
- Cumulative Distribution Function
- CDF

---

## Tags
#cumulativeprobability #cdf #probability #statistics #randomvariables

---

## Links to Explore
- [[Probability Distributions]]: Learn how CDFs describe random variables.
- [[Probability Density Function (PDF)]]: Explore the relationship between CDF and PDF.
- [[Probability Mass Function (PMF)]]: Compare the CDF for discrete and continuous cases.
- [[Quantiles]]: Use the CDF to compute specific quantiles.