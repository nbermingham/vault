## Overview
The **Poisson Distribution** is a discrete probability distribution that models the number of events occurring in a fixed interval of time, space, or other continuous domains when events occur independently and at a constant average rate. It is widely used in [[Probability]] and [[Statistics]] for count-based phenomena.

The distribution is parameterized by $\lambda$, the average number of events per interval, and is defined by the formula:
$$
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}, \, k = 0, 1, 2, \dots
$$
Where:
- $X$: The random variable representing the number of events.
- $\lambda$: The average rate of occurrence.
- $e$: Euler's number ($\approx 2.718$).
- $k!$: Factorial of $k$.

---

## Key Properties

1. **[[Discrete Distribution]]**:
   - $X$ takes non-negative integer values: $k = 0, 1, 2, \dots$.

2. **Mean and Variance**:
   - The mean and variance of the Poisson Distribution are equal:
     $$
     E[X] = \lambda, \quad \text{Var}(X) = \lambda
     $$

3. **[[Memoryless]] Property**:
   - Similar to the [[Exponential Distribution]] (its continuous counterpart), the Poisson process is memoryless.

4. **[[Additive Property]]**:
   - If $X_1 \sim \text{Poisson}(\lambda_1)$ and $X_2 \sim \text{Poisson}(\lambda_2)$, then:
     $$
     X_1 + X_2 \sim \text{Poisson}(\lambda_1 + \lambda_2)
     $$

---

## Assumptions

1. **[[Independence]]**:
   - Events occur independently of one another.

2. **Constant Rate ($\lambda$)**:
   - The average rate of occurrence $\lambda$ is constant over time or space.

3. **No Simultaneous Events**:
   - Two or more events cannot occur at the exact same instant.

---

## Applications

1. **Queueing Theory**:
   - Model customer arrivals at a service counter.

2. **Epidemiology**:
   - Count the number of disease cases in a given time or region.

3. **Traffic Flow**:
   - Predict the number of cars passing through an intersection in a fixed time.

4. **Call Centers**:
   - Estimate the number of incoming calls per hour.

5. **Quality Control**:
   - Count the number of defects on a product in manufacturing.

---

## Example

### Customer Arrivals
Suppose a coffee shop averages 3 customers arriving per hour ($\lambda = 3$). The probability of exactly 5 customers arriving in an hour is:
$$
P(X = 5) = \frac{3^5 e^{-3}}{5!} = \frac{243 \cdot 0.0498}{120} \approx 0.102
$$

---

## Tools and Libraries

1. **Python**:
   - **SciPy**: `scipy.stats.poisson` for Poisson calculations.
   - **NumPy**: Generate Poisson-distributed random samples with `numpy.random.poisson`.
2. **R**:
   - Use `dpois()` for PMF and `rpois()` for random sampling.

---

## Related Topics

- [[Probability Distributions]]: The Poisson Distribution is a key discrete distribution.
- [[Exponential Distribution]]: The continuous counterpart of the Poisson Distribution.
- [[Binomial Distribution]]: For large $n$ and small $p$, it approximates the Poisson Distribution.
- [[Random Variables]]: Poisson describes a discrete random variable.

---

## Aliases
- Poisson Distribution
- Poisson Process

---

## Tags
#poissondistribution #probability #statistics #randomvariables #discretedistributions

---

## Links to Explore
- [[Probability Distributions]]: Learn how the Poisson fits among other distributions.
- [[Exponential Distribution]]: Explore its relationship with the Poisson process.
- [[Binomial Distribution]]: Understand the conditions under which it approximates the Poisson.
- [[Random Variables]]: Investigate how Poisson distributions describe discrete random variables.
- [[Statistics]]: Discover applications of the Poisson Distribution in data analysis.