## Overview
The **Binomial Distribution** is a discrete probability distribution that models the number of successes in a fixed number of independent Bernoulli trials. Each trial has two possible outcomes: success or failure, with a constant probability of success. It is widely used in [[Probability]] and [[Statistics]] to model binary events.

---

## Key Concepts

1. **[[Bernoulli Distribution|Bernoulli Trial]]**:
   - A random experiment with two outcomes: success (1) and failure (0).
   - Example: Flipping a coin (success = heads, failure = tails).

2. **Parameters**:
   - $n$: Number of trials.
   - $p$: Probability of success in each trial.

3. **[[Probability Mass Function (PMF)]]**:
   - The probability of observing exactly $k$ successes in $n$ trials is given by:
     $$
     P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}
     $$
     Where:
     - $\binom{n}{k} = \frac{n!}{k!(n-k)!}$ is the binomial coefficient.

4. **[[Cumulative Distribution Function (CDF)]]**:
   - The probability of observing $k$ or fewer successes:
     $$
     P(X \leq k) = \sum_{i=0}^k \binom{n}{i} p^i (1-p)^{n-i}
     $$

---

## Properties

1. **[[Expected Value]] (Mean)**:
   - $$
     E[X] = n \cdot p
     $$

2. **[[Variance]]**:
   - $$
     \text{Var}(X) = n \cdot p \cdot (1-p)
     $$

3. **Shape**:
   - Symmetric if $p = 0.5$, skewed to the right if $p < 0.5$, and skewed to the left if $p > 0.5$.

---

## Assumptions

1. **Fixed Number of Trials**:
   - The number of trials $n$ is predetermined.
2. **Independent Trials**:
   - The outcome of one trial does not affect the outcome of another.
3. **Constant Probability**:
   - The probability of success $p$ remains the same for all trials.

---

## Applications

1. **Quality Control**:
   - Model the number of defective items in a batch.
2. **Medical Studies**:
   - Estimate the probability of recovery after treatment.
3. **Finance**:
   - Predict the number of successful investments in a portfolio.
4. **Sports**:
   - Model the number of successful free throws in basketball.

---

## Example

### Coin Toss
Suppose a fair coin is tossed 10 times ($n = 10$, $p = 0.5$):
1. What is the probability of getting exactly 6 heads ($k = 6$)?
   $$
   P(X = 6) = \binom{10}{6} (0.5)^6 (0.5)^4 = \frac{10!}{6!4!} (0.5)^{10} = 0.205
   $$

2. What is the expected number of heads?
   $$
   E[X] = n \cdot p = 10 \cdot 0.5 = 5
   $$

---

## Related Topics

- [[Bernoulli Distribution]]: The building block of the binomial distribution.
- [[Poisson Distribution]]: Approximation of the binomial distribution for rare events.
- [[Probability Distributions]]: Explore other discrete and continuous distributions.
- [[Random Variables]]: Understand the foundation of the binomial distribution.
- [[Statistics]]: Applications of the binomial distribution in data analysis.

---

## Aliases
- Binomial Distribution
- Discrete Binomial

---

## Tags
#binomialdistribution #probability #statistics #randomvariables #discretedistributions

---

## Links to Explore
- [[Bernoulli Distribution]]: Learn about the fundamental building block of the binomial distribution.
- [[Poisson Distribution]]: Understand its relationship to the binomial distribution.
- [[Probability Distributions]]: Discover other distributions used in probability and statistics.
- [[Random Variables]]: Explore how binomial distributions are defined as discrete random variables.
- [[Statistics]]: Investigate how the binomial distribution is applied in data analysis.