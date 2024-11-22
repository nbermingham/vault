## Overview
**Probability Distributions** describe how probabilities are assigned to the possible outcomes of a random variable. They provide a mathematical framework for understanding and modeling uncertainty in [[Probability]] and [[Statistics]]. Distributions are classified into two main types: [[Discrete Distributions]] and [[Continuous Distributions]].

---

## Types of Probability Distributions

1. **Discrete Distributions**:
   - Applicable to random variables with countable outcomes.
   - Defined by a [[Probability Mass Function (PMF)]].
   - Examples:
     - [[Bernoulli Distribution]]: Single binary trial.
     - [[Binomial Distribution]]: Number of successes in $n$ trials.
     - [[Poisson Distribution]]: Count of events in a fixed interval.

2. **Continuous Distributions**:
   - Applicable to random variables with uncountable outcomes (e.g., real numbers).
   - Defined by a [[Probability Density Function (PDF)]].
   - Examples:
     - [[Normal Distribution]]: Bell-shaped curve for symmetric data.
     - [[Exponential Distribution]]: Time between events in a Poisson process.
     - [[Gamma Distribution]]: Generalized exponential distribution.

---

## Key Concepts

1. **PMF and PDF**:
   - [[Probability Mass Function (PMF)]]: For discrete random variables.
   - [[Probability Density Function (PDF)]]: For continuous random variables.

2. **Cumulative Distribution Function (CDF)**:
   - Describes the probability that a random variable takes on a value less than or equal to $x$:
     $$
     F(x) = P(X \leq x)
     $$
   - Applies to both discrete and continuous distributions.

3. **Parameters**:
   - Distributions are parameterized by values such as:
     - Mean ($\mu$): Center of the distribution.
     - Variance ($\sigma^2$): Spread of the distribution.
     - Rate ($\lambda$): Frequency of events (e.g., Poisson and Exponential).

4. **Moments**:
   - [[Expectation]]: Mean of the random variable.
   - [[Variance]]: Measure of spread.
   - Higher-order moments (e.g., skewness and kurtosis).

---

## Applications

1. **Modeling Uncertainty**:
   - Distributions model real-world phenomena like heights, test scores, or wait times.
2. **Hypothesis Testing**:
   - Distributions like [[Normal Distribution]] and [[t-Distribution]] are used for statistical tests.
3. **Machine Learning**:
   - Probabilistic models rely on distributions to calculate likelihoods.
4. **Econometrics**:
   - Analyze financial risks and returns using distributions.
5. **Reliability Analysis**:
   - Model time-to-failure with distributions like [[Exponential Distribution]].

---

## Examples

### Discrete Distribution: Binomial
- A coin is flipped 10 times. The number of heads follows a [[Binomial Distribution]] with:
  - $n = 10$ (trials)
  - $p = 0.5$ (probability of success per trial).

### Continuous Distribution: Normal
- The heights of individuals in a population are often modeled by a [[Normal Distribution]] with:
  - Mean ($\mu$): Average height.
  - Variance ($\sigma^2$): Variability in height.

---

## Related Topics

- [[Random Variables]]: Distributions describe the behavior of random variables.
- [[Probability Density Function (PDF)]]: For continuous distributions.
- [[Probability Mass Function (PMF)]]: For discrete distributions.
- [[Cumulative Distribution Function (CDF)]]: Cumulative probability for distributions.
- [[Expectation]]: Calculating the mean using a distribution.

---

## Aliases
- Probability Distributions
- Probability Models

---

## Tags
#probabilitydistributions #probability #statistics #randomvariables #machinelearning

---

## Links to Explore
- [[Discrete Distributions]]: Explore distributions for countable outcomes.
- [[Continuous Distributions]]: Learn about distributions over real numbers.
- [[Binomial Distribution]]: A key discrete distribution.
- [[Normal Distribution]]: The most widely used continuous distribution.
- [[Random Variables]]: Discover how distributions describe random variables.