## Overview
A **Probability Mass Function (PMF)** is a mathematical function that provides the probability of a discrete random variable taking on a specific value. It is a core concept in [[Probability]] and forms the foundation for understanding [[Discrete Distributions]] like the [[Bernoulli Distribution]] and [[Binomial Distribution]].

The PMF is defined as:
$$
P(X = x) = f(x)
$$
Where:
- $X$: A discrete random variable.
- $x$: A specific value that $X$ can take.
- $f(x)$: The probability of $X$ taking the value $x$.

---

## Key Properties

1. **Non-Negativity**:
   - $P(X = x) \geq 0$ for all $x$.

2. **Normalization**:
   - The sum of all probabilities over the sample space equals 1:
     $$
     \sum_{x \in \Omega} P(X = x) = 1
     $$

3. **Discreteness**:
   - PMFs are defined only for discrete random variables.

---

## Applications

1. **Modeling Discrete Random Variables**:
   - PMFs describe distributions like the [[Bernoulli Distribution]], [[Binomial Distribution]], and [[Poisson Distribution]].

2. **Risk Analysis**:
   - Determine probabilities of specific outcomes in risk assessments.

3. **Machine Learning**:
   - PMFs are used in classification problems to model class probabilities.

4. **Decision Making**:
   - Help in probabilistic reasoning, such as in [[Bayesian Inference]].

---

## Example

### Coin Toss ([[Bernoulli Distribution]])
For a fair coin toss, the random variable $X$ represents the outcome:
- $X = 1$ (Heads): $P(X = 1) = 0.5$
- $X = 0$ (Tails): $P(X = 0) = 0.5$

The PMF is:
$$
P(X = x) = 
\begin{cases} 
0.5 & \text{if } x \in \{0, 1\} \\
0 & \text{otherwise}
\end{cases}
$$

---

### Rolling a Die ([[Uniform Distribution]])
For a six-sided die:
- Sample space: $\Omega = \{1, 2, 3, 4, 5, 6\}$
- PMF: $P(X = x) = \frac{1}{6}$ for $x \in \{1, 2, 3, 4, 5, 6\}$

---

## Related Topics

- [[Probability Distributions]]: Frameworks for defining PMFs.
- [[Cumulative Distribution Function (CDF)]]: Summarizes probabilities up to a given value.
- [[Random Variables]]: PMFs are used to describe discrete random variables.
- [[Bernoulli Distribution]]: A basic example of a PMF.
- [[Discrete Distributions]]: PMFs are central to understanding these distributions.

---

## Aliases
- Probability Mass Function
- PMF
- Discrete Probability Function

---

## Tags
#pmf #probability #statistics #randomvariables #discretedistributions

---

## Links to Explore
- [[Random Variables]]: Learn how PMFs are used to define them.
- [[Probability Distributions]]: Explore distributions with associated PMFs.
- [[Bernoulli Distribution]]: A fundamental example of a PMF.
- [[Binomial Distribution]]: A more complex distribution described by a PMF.
- [[Cumulative Distribution Function (CDF)]]: Compare how CDF extends PMF.