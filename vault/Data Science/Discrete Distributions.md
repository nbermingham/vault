## Overview
**Discrete Distributions** describe the probability of outcomes for a discrete random variable, where the variable can take on a countable number of distinct values. These distributions are characterized by a [[Probability Mass Function (PMF)]], which assigns probabilities to each possible value. Discrete distributions are foundational in [[Probability]] and [[Statistics]] for modeling events like counts, successes, and failures.

---

## Key Properties

1. **Countable Outcomes**:
   - The random variable can only take on distinct, separate values.
   - Example: Rolling a die produces one of $\{1, 2, 3, 4, 5, 6\}$.

2. **Normalization**:
   - The sum of all probabilities equals 1:
     $$
     \sum_{x \in \Omega} P(X = x) = 1
     $$

3. **Defined by a PMF**:
   - Probabilities are assigned to each possible value of the random variable.

---

## Common Discrete Distributions

1. **[[Bernoulli Distribution]]**:
   - Models a single trial with two outcomes: success (1) and failure (0).
   - Example: Tossing a coin.

2. **[[Binomial Distribution]]**:
   - Describes the number of successes in $n$ independent Bernoulli trials.
   - Example: Number of heads in 10 coin tosses.

3. **[[Poisson Distribution]]**:
   - Models the number of events occurring in a fixed interval of time or space.
   - Example: Number of customer arrivals at a store in an hour.

4. **[[Geometric Distribution]]**:
   - Models the number of trials needed to get the first success.
   - Example: Flipping a coin until the first heads.

5. **[[Hypergeometric Distribution]]**:
   - Models the number of successes in a sample drawn without replacement.
   - Example: Drawing defective items from a batch.

6. **[[Uniform Distribution (Discrete)]]**:
   - All outcomes have equal probability.
   - Example: Rolling a fair die.

---

## Applications

1. **Quality Control**:
   - Use the [[Binomial Distribution]] to model the number of defective items in a batch.
2. **Queueing Theory**:
   - Use the [[Poisson Distribution]] to model the arrival of customers.
3. **Risk Analysis**:
   - Model the probability of certain events, such as accidents or defaults.
4. **Machine Learning**:
   - Model probabilities in classification tasks, such as [[Naive Bayes]].

---

## Example

### Rolling a Die (Uniform Distribution)
For a fair six-sided die:
- Sample space: $\Omega = \{1, 2, 3, 4, 5, 6\}$
- PMF: $P(X = x) = \frac{1}{6}$ for $x \in \{1, 2, 3, 4, 5, 6\}$

### Number of Heads in 10 Coin Tosses (Binomial Distribution)
For $n = 10$, $p = 0.5$:
- Probability of exactly 4 heads:
  $$
  P(X = 4) = \binom{10}{4} (0.5)^4 (0.5)^6
  $$

---

## Challenges

1. **Complex Relationships**:
   - Some distributions, like the [[Hypergeometric Distribution]], require additional parameters and assumptions.
2. **Overlapping Use Cases**:
   - Choosing the right distribution for a specific problem may require domain expertise.

---

## Related Topics

- [[Probability Distributions]]: Discrete distributions are one type of probability distribution.
- [[Probability Mass Function (PMF)]]: Defines probabilities for discrete distributions.
- [[Random Variables]]: Discrete distributions describe discrete random variables.
- [[Cumulative Distribution Function (CDF)]]: Summarizes probabilities for discrete distributions.
- [[Continuous Distributions]]: Compare discrete distributions to their continuous counterparts.

---

## Aliases
- Discrete Distributions
- Discrete Probability Distributions

---

## Tags
#discretedistributions #probability #statistics #randomvariables #pmf

---

## Links to Explore
- [[Probability Mass Function (PMF)]]: Understand how discrete probabilities are assigned.
- [[Bernoulli Distribution]]: Explore the simplest discrete distribution.
- [[Binomial Distribution]]: Learn about modeling multiple trials with discrete outcomes.
- [[Poisson Distribution]]: Understand its application in count-based events.
- [[Random Variables]]: Investigate how discrete distributions define random variables.