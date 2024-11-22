## Overview
**Linearity of Expectation** is a key property in [[Probability]] that states the expected value of a sum of random variables is equal to the sum of their expected values, regardless of whether the variables are independent. This property simplifies calculations involving multiple random variables and is widely used in [[Statistics]] and [[Machine Learning]].

Mathematically, for random variables $X_1, X_2, \dots, X_n$:
$$
E\left[\sum_{i=1}^n X_i\right] = \sum_{i=1}^n E[X_i]
$$

---

## Key Properties

1. **Additivity**:
   - The expectation of a sum is the sum of the expectations:
     $$
     E[X + Y] = E[X] + E[Y]
     $$

2. **Scaling**:
   - Constants can be factored out of the expectation:
     $$
     E[aX] = aE[X]
     $$
     Where $a$ is a constant.

3. **No Independence Required**:
   - Linearity holds whether or not the random variables are independent.

4. **Combination**:
   - For random variables $X$ and $Y$:
     $$
     E[aX + bY] = aE[X] + bE[Y]
     $$
     Where $a$ and $b$ are constants.

---

## Applications

1. **Simplifying Calculations**:
   - Easily compute the expected value of complex sums or weighted sums of random variables.

2. **Machine Learning**:
   - Optimize models by breaking down expectations in [[Loss Functions]] (e.g., [[Mean Squared Error]], [[Cross-Entropy Loss]]).

3. **Game Theory**:
   - Compute expected payoffs in probabilistic games.

4. **Finance**:
   - Calculate expected returns of portfolios by summing weighted expected values of individual assets.

---

## Examples

### Example 1: Sum of Dice Rolls
Let $X_1$ and $X_2$ represent the outcomes of two six-sided dice. Each die has:
- $E[X_1] = E[X_2] = 3.5$

The total expected value of the sum $S = X_1 + X_2$ is:
$$
E[S] = E[X_1] + E[X_2] = 3.5 + 3.5 = 7
$$

### Example 2: Weighted Sum of Test Scores
Suppose $X_1, X_2, X_3$ are test scores, and their weights are $w_1, w_2, w_3$. The weighted sum is:
$$
Y = w_1X_1 + w_2X_2 + w_3X_3
$$
The expected value is:
$$
E[Y] = w_1E[X_1] + w_2E[X_2] + w_3E[X_3]
$$

---

## Limitations

1. **Does Not Apply to Variance**:
   - Linearity applies only to expectations, not to [[Variance]]. For variance, independence is required:
     $$
     \text{Var}(X + Y) = \text{Var}(X) + \text{Var}(Y) \, \text{if } X, Y \text{ are independent.}
     $$

2. **Requires Finite Expectations**:
   - The property holds only when $E[X]$ and $E[Y]$ are finite.

---

## Related Topics

- [[Expected Value]]: Linearity of expectation builds on the concept of expectation.
- [[Variance]]: Understand how variability interacts with expectation.
- [[Random Variables]]: Core entities over which linearity is applied.
- [[Probability Distributions]]: Distributions define the expectations used in linearity.

---

## Aliases
- Linearity of Expectation
- Additivity of Expectation
- Linear Expectation

---

## Tags
#linearityofexpectation #probability #statistics #randomvariables #machinelearning

---

## Links to Explore
- [[Expected Value]]: Learn the foundational concept behind linearity.
- [[Variance]]: Contrast how variance behaves differently from expectation.
- [[Probability Distributions]]: Discover how distributions define expectations.
- [[Random Variables]]: Explore how expectations are computed over these variables.