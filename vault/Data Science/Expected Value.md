---
aliases:
  - Expectation
  - EV
---
## Overview
**Expected Value** (or **Mean**) is a fundamental concept in [[Probability]] and [[Statistics]] that represents the average or center of a random variable's distribution. It quantifies the long-term average outcome of a random process if repeated many times. Expected value is used extensively in [[Machine Learning]], [[Econometrics]], and decision-making under uncertainty.

The formula for expected value depends on whether the random variable is discrete or continuous.

---

## Key Formulas

1. **Discrete Random Variable**:
   $$
   E[X] = \sum_{x \in \Omega} x \cdot P(X = x)
   $$
   Where:
   - $X$: Random variable.
   - $P(X = x)$: [[Probability Mass Function (PMF)]] for discrete $X$.
   - $\Omega$: Sample space (all possible outcomes).

2. **Continuous Random Variable**:
   $$
   E[X] = \int_{-\infty}^\infty x \cdot f(x) \, dx
   $$
   Where:
   - $f(x)$: [[Probability Density Function (PDF)]] for continuous $X$.

---

## Properties

1. **Linearity of Expectation**:
   - For any two random variables $X$ and $Y$, and constants $a$ and $b$:
     $$
     E[aX + bY] = aE[X] + bE[Y]
     $$

2. **Expectation of Constants**:
   - If $c$ is a constant:
     $$
     E[c] = c
     $$

3. **Independence**:
   - If $X$ and $Y$ are independent:
     $$
     E[XY] = E[X] \cdot E[Y]
     $$

---

## Applications

1. **Risk Analysis**:
   - Compute the expected profit or loss in finance and insurance.
2. **Machine Learning**:
   - Optimize models by minimizing expected loss (e.g., [[Cross-Entropy Loss]]).
3. **Decision Theory**:
   - Use expected utility to guide decision-making.
4. **Game Theory**:
   - Calculate average outcomes in probabilistic games.

---

## Examples

### Discrete Example (Rolling a Die)
Let $X$ be the outcome of rolling a six-sided die:
- Sample space: $\Omega = \{1, 2, 3, 4, 5, 6\}$
- $P(X = x) = \frac{1}{6}$ for all $x$.

The expected value is:
$$
E[X] = \sum_{x=1}^6 x \cdot P(X = x) = \frac{1+2+3+4+5+6}{6} = 3.5
$$

### Continuous Example (Exponential Distribution)
Let $X$ follow an [[Exponential Distribution]] with rate parameter $\lambda = 2$. The expected value is:
$$
E[X] = \int_0^\infty x \cdot (2e^{-2x}) \, dx = \frac{1}{2}
$$

---

## Related Topics

- [[Variance]]: Measures the spread of a random variable around its expected value.
- [[Random Variables]]: The expected value is a key property of random variables.
- [[Probability Distributions]]: Define the probabilities needed to compute expected value.
- [[Linearity of Expectation]]: A useful property for simplifying calculations.
- [[Cumulative Distribution Function (CDF)]]: Integrates into expected value for continuous variables.

---

## Aliases
- Expected Value
- Mean
- Expectation
- Mathematical Expectation

---

## Tags
#expectedvalue #probability #statistics #randomvariables #machinelearning

---

## Links to Explore
- [[Variance]]: Understand how variability relates to the expected value.
- [[Random Variables]]: Discover how expected value characterizes random variables.
- [[Probability Distributions]]: Explore distributions used to compute expected value.
- [[Linearity of Expectation]]: Learn a critical property for simplifying expectations.
- [[Cumulative Distribution Function (CDF)]]: Connect with the integration process in continuous cases.