---
aliases:
  - Bernoulli Trial
---
## Overview
The **Bernoulli Distribution** is the simplest discrete probability distribution, modeling a single trial that has exactly two outcomes: success (1) or failure (0). It is foundational in [[Probability]] and serves as the building block for more complex distributions like the [[Binomial Distribution]].

---

## Key Concepts

1. **Parameters**:
   - $p$: Probability of success.
   - $1-p$: Probability of failure.

2. **[[Probability Mass Function (PMF)]]**:
   - The probability of observing success ($X = 1$) or failure ($X = 0$) is given by:
     $$
     P(X = x) = p^x (1-p)^{1-x}, \, x \in \{0, 1\}
     $$
     Where:
     - $x = 1$: Success.
     - $x = 0$: Failure.

3. **Expected Value (Mean)**:
   - $$
     E[X] = p
     $$

4. **Variance**:
   - $$
     \text{Var}(X) = p \cdot (1-p)
     $$

---

## Properties

1. **Discrete Distribution**:
   - Takes on only two values: 0 and 1.

2. **Independent Trials**:
   - Assumes independence between multiple Bernoulli trials.

3. **Special Case of Binomial Distribution**:
   - A [[Binomial Distribution]] with $n=1$ is a Bernoulli distribution.

---

## Applications

1. **Coin Toss**:
   - Models a single coin toss (success = heads, failure = tails).

2. **Customer Behavior**:
   - Whether a customer clicks on an ad (success) or not (failure).

3. **Quality Control**:
   - Whether a product is defective (failure) or non-defective (success).

4. **Medical Studies**:
   - Whether a treatment results in recovery (success) or no recovery (failure).

---

## Example

### Fair Coin Toss
If the probability of heads (success) is $p = 0.5$, then:
- $P(X = 1) = 0.5$
- $P(X = 0) = 1 - 0.5 = 0.5$

The expected value is:
$$
E[X] = p = 0.5
$$

And the variance is:
$$
\text{Var}(X) = p \cdot (1-p) = 0.5 \cdot 0.5 = 0.25
$$

---

## Related Topics

- [[Binomial Distribution]]: Models multiple independent Bernoulli trials.
- [[Probability Distributions]]: Explore other foundational distributions.
- [[Random Variables]]: Bernoulli distributions are discrete random variables.
- [[Statistics]]: Bernoulli processes are commonly studied in data analysis.

---

## Aliases
- Bernoulli Distribution
- Bernoulli Trial

---

## Tags
#bernoullidistribution #probability #statistics #randomvariables #discretedistributions

---

## Links to Explore
- [[Binomial Distribution]]: Understand how it generalizes multiple Bernoulli trials.
- [[Probability Distributions]]: Discover other discrete and continuous distributions.
- [[Random Variables]]: Explore the role of Bernoulli distributions in probability theory.
- [[Statistics]]: Investigate applications of Bernoulli distributions in data analysis.