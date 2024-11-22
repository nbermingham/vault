---
aliases:
  - PDF
  - Probability Density Function
  - probability density function
---
## Overview
A **Probability Density Function (PDF)** represents the likelihood of a continuous random variable taking on a specific value within an interval. It is a fundamental concept in [[Probability]] and [[Statistics]], describing the distribution of probabilities over a continuous range of values.

The PDF is defined as:
$$
f(x) = \frac{dF(x)}{dx}
$$
Where:
- $f(x)$: The probability density at $x$.
- $F(x)$: The [[Cumulative Distribution Function (CDF)]].
- $x$: A specific value of the random variable.

While the value of the PDF at any single point does not represent a probability (it can exceed 1), the area under the curve within an interval does.

---

## Properties

1. **Non-Negativity**:
   - $f(x) \geq 0$ for all $x$.

2. **Normalization**:
   - The total area under the curve equals 1:
     $$
     \int_{-\infty}^\infty f(x) \, dx = 1
     $$

3. **Relationship with CDF**:
   - The PDF is the derivative of the CDF:
     $$
     f(x) = \frac{dF(x)}{dx}
     $$

4. **Probability for an Interval**:
   - The probability that the random variable falls within an interval $[a, b]$ is given by:
     $$
     P(a \leq X \leq b) = \int_a^b f(x) \, dx
     $$

---

## Applications

1. **Describing Continuous Distributions**:
   - The PDF defines distributions like the [[Normal Distribution]], [[Exponential Distribution]], and [[Gamma Distribution]].

2. **Modeling Real-World Phenomena**:
   - PDFs describe distributions of data like heights, weights, or time durations.

3. **Machine Learning**:
   - Used in probabilistic models to calculate likelihoods.

4. **Statistical Inference**:
   - PDFs form the basis for parameter estimation in distributions.

---

## Example

### Normal Distribution
The PDF of a Normal Distribution with mean $\mu$ and variance $\sigma^2$ is:
$$
f(x) = \frac{1}{\sqrt{2\pi\sigma^2}} e^{-\frac{(x - \mu)^2}{2\sigma^2}}
$$
Key properties:
- Symmetric around $\mu$.
- Bell-shaped curve.

### Exponential Distribution
The PDF of an Exponential Distribution with rate $\lambda$ is:
$$
f(x) = \lambda e^{-\lambda x}, \, x \geq 0
$$
Key properties:
- Skewed to the right.
- Models waiting times between events.

---

## Related Topics

- [[Probability Distributions]]: Frameworks for describing random variables using PDFs.
- [[Cumulative Distribution Function (CDF)]]: The integral of the PDF.
- [[Random Variables]]: PDFs describe the behavior of continuous random variables.
- [[Expectation]]: Calculating the mean of a distribution using the PDF.
- [[Variance]]: Measuring the spread of a distribution using the PDF.

---

## Aliases
- Probability Density Function
- PDF
- Density Function

---

## Tags
#probabilitydensityfunction #pdf #probability #statistics #continuousdistributions

---

## Links to Explore
- [[Cumulative Distribution Function (CDF)]]: Explore the relationship between CDF and PDF.
- [[Probability Distributions]]: Learn how PDFs define continuous distributions.
- [[Normal Distribution]]: A widely used PDF in statistics.
- [[Exponential Distribution]]: An example of a skewed PDF.
- [[Expectation]]: Compute averages using the PDF.