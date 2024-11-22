## Overview
A **Random Variable** is a mathematical concept in [[Probability]] that assigns numerical values to the outcomes of a random experiment. It provides a way to quantify uncertainty and is central to [[Statistics]] and many [[Machine Learning]] algorithms. Random variables can be classified as discrete or continuous.

---

## Types of Random Variables

1. **Discrete Random Variable**:
   - Takes on a countable set of distinct values.
   - Example: Number of heads in 10 coin tosses.
   - Common distributions: [[Binomial Distribution]], [[Poisson Distribution]].

2. **Continuous Random Variable**:
   - Takes on an uncountable range of values, often within an interval.
   - Example: Height of individuals in a population.
   - Common distributions: [[Normal Distribution]], [[Exponential Distribution]].

---

## Key Concepts

1. **[[Probability Mass Function (PMF)]]**:
   - For discrete random variables, the PMF gives the probability of each specific value:
     $$
     P(X = x) = p(x)
     $$

2. **[[Probability Density Function (PDF)]]**:
   - For continuous random variables, the PDF describes the likelihood of a value within an interval:
     $$
     P(a \leq X \leq b) = \int_a^b f(x) \, dx
     $$

3. **[[Cumulative Distribution Function (CDF)]]**:
   - Describes the probability that the random variable is less than or equal to a given value:
     $$
     F(x) = P(X \leq x)
     $$

4. **Expected Value (Mean)**:
   - The long-term average or "center" of the random variable:
     $$
     E[X] = \begin{cases} 
     \sum_x x \cdot P(X = x), & \text{if discrete} \\ 
     \int_{-\infty}^{\infty} x \cdot f(x) \, dx, & \text{if continuous}
     \end{cases}
     $$

5. **Variance**:
   - Measures the spread or variability of the random variable:
     $$
     \text{Var}(X) = E[(X - E[X])^2]
     $$

---

## Applications

1. **Statistics**:
   - Forms the foundation of statistical inference (e.g., estimating population parameters).
2. **Machine Learning**:
   - Used in probabilistic models like [[Naive Bayes]] and [[Bayesian Inference]].
3. **Finance**:
   - Models stock prices, risks, and returns as random variables.
4. **Physics**:
   - Quantifies uncertainty in measurements and predictions.
5. **Operations Research**:
   - Models random processes in supply chains and logistics.

---

## Example

### Discrete Random Variable
Consider rolling a fair six-sided die:
- Sample space: $\Omega = \{1, 2, 3, 4, 5, 6\}$.
- PMF: $P(X = k) = \frac{1}{6}$ for $k \in \{1, 2, 3, 4, 5, 6\}$.
- Expected value:
  $$
  E[X] = \sum_{k=1}^6 k \cdot P(X = k) = \frac{1+2+3+4+5+6}{6} = 3.5
  $$

---

## Key Properties

1. **Independence**:
   - Two random variables $X$ and $Y$ are independent if:
     $$
     P(X \cap Y) = P(X)P(Y)
     $$

2. **Linearity of Expectation**:
   - The expectation of a sum of random variables is the sum of their expectations:
     $$
     E[X + Y] = E[X] + E[Y]
     $$

---

## Related Topics

- [[Probability]]: The foundation for understanding random variables.
- [[Probability Distributions]]: Frameworks for describing random variables.
- [[Expected Value]]: Key measure for understanding the central tendency.
- [[Variance]]: Describes the spread of a random variable.
- [[Bayesian Inference]]: Applies random variables to update beliefs.

---

## Aliases
- Random Variable
- Stochastic Variable
- RV

---

## Tags
#randomvariable #probability #statistics #machinelearning #inference

---

## Links to Explore
- [[Probability]]: Understand the broader context of random variables.
- [[Probability Distributions]]: Explore how distributions define random variables.
- [[Expected Value]]: Learn how the mean is computed for random variables.
- [[Variance]]: Discover how variability is quantified.
- [[Bayesian Inference]]: See how random variables are applied in Bayesian reasoning.