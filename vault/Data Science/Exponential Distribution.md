## Overview
The **Exponential Distribution** is a continuous probability distribution commonly used to model the time between events in a Poisson process. It describes the time until the next event occurs when events happen independently and at a constant rate. The distribution is characterized by its rate parameter $\lambda$ (or mean $\mu = \frac{1}{\lambda}$).

The [[Probability Density Function (PDF)]] is:
$$
f(x; \lambda) = \begin{cases} 
\lambda e^{-\lambda x}, & x \geq 0 \\
0, & x < 0
\end{cases}
$$
Where:
- $x$: Time until the next event.
- $\lambda$: Rate parameter (average number of events per unit time).

---

## Key Properties

1. **[[Memorylessness]]**:
   - The Exponential Distribution is memoryless, meaning the probability of an event occurring in the future does not depend on when the last event occurred:
     $$
     P(X > t + s | X > t) = P(X > s)
     $$

2. **Mean and Variance**:
   - Mean (expected value):
     $$
     E[X] = \frac{1}{\lambda}
     $$
   - Variance:
     $$
     \text{Var}(X) = \frac{1}{\lambda^2}
     $$

3. **[[Cumulative Distribution Function (CDF)]]**:
   - The probability that the event occurs within time $t$:
     $$
     F(x; \lambda) = P(X \leq x) = \begin{cases}
     1 - e^{-\lambda x}, & x \geq 0 \\
     0, & x < 0
     \end{cases}
     $$

---

## Assumptions

1. **Independent Events**:
   - Events occur independently of one another.
2. **Constant Rate ($\lambda$)**:
   - Events occur at a constant average rate over time.

---

## Applications

1. **Queueing Theory**:
   - Model waiting times between customer arrivals.
2. **Reliability Analysis**:
   - Estimate the time to failure for systems or components.
3. **Telecommunications**:
   - Model the time between data packet arrivals.
4. **Biology**:
   - Model the time until the next biological event occurs, such as cell division.

---

## Example

### Customer Arrival Time
Suppose customers arrive at a rate of 2 per hour ($\lambda = 2$). The probability that the next customer arrives within 30 minutes ($x = 0.5$ hours) is:
$$
P(X \leq 0.5) = 1 - e^{-\lambda x} = 1 - e^{-2 \cdot 0.5} = 1 - e^{-1} \approx 0.632
$$

---

## Tools and Libraries

1. **Python**:
   - **SciPy**: Use `scipy.stats.expon` for calculations.
   - **NumPy**: Generate random samples with `numpy.random.exponential`.
2. **R**:
   - Use `dexp()` for the [[Probability Density Function (PDF)|PDF]] and `pexp()` for the [[Cumulative Distribution Function (CDF)|CDF]].

---

## Related Topics

- [[Poisson Distribution]]: The Exponential Distribution models the time between events in a Poisson process.
- [[Continuous Distributions]]: The Exponential Distribution is a key continuous distribution.
- [[Gamma Distribution]]: The Exponential Distribution is a special case of the Gamma Distribution with shape parameter $\alpha = 1$.
- [[Statistics]]: Used in survival analysis and reliability studies.

---

## Aliases
- Exponential Distribution
- Waiting Time Distribution

---

## Tags
#exponentialdistribution #probability #statistics #continuousdistributions #poissonprocess

---

## Links to Explore
- [[Poisson Distribution]]: Understand its relationship with the Exponential Distribution.
- [[Continuous Distributions]]: Explore other continuous probability distributions.
- [[Gamma Distribution]]: Learn how the Exponential Distribution is a special case.
- [[Statistics]]: Discover how the Exponential Distribution is applied in data analysis.