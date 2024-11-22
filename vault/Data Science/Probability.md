## Overview
**Probability** is a branch of [[Mathematics]] that quantifies the likelihood of an event occurring. It forms the foundation of [[Statistics]] and many [[Machine Learning]] algorithms, enabling us to model uncertainty and randomness. Probability values range between 0 (impossible event) and 1 (certain event).

---

## Key Concepts

1. **[[Random Experiment]]**:
   - An experiment or process with an uncertain outcome (e.g., rolling a die, flipping a coin).

2. **[[Sample Space]] ($\Omega$)**:
   - The set of all possible outcomes of a random experiment.
   - Example: For a coin toss, $\Omega = \{Heads, Tails\}$.

3. **[[Event]]**:
   - A subset of the sample space. It represents one or more outcomes.
   - Example: Rolling an even number on a die ($\{2, 4, 6\}$).

4. **Probability of an Event ($P(A)$)**:
   - The measure of the likelihood that event $A$ occurs:
     $$
     P(A) = \frac{\text{Number of favorable outcomes}}{\text{Total number of outcomes}}
     $$

---

## Types of Probability

1. **[[Theoretical Probability]]**:
   - Based on reasoning and mathematical models.
   - Example: The probability of rolling a 6 on a fair die is $\frac{1}{6}$.

2. **[[Empirical Probability]]**:
   - Based on observed data or experiments:
     $$
     P(A) = \frac{\text{Number of times } A \text{ occurs}}{\text{Total number of trials}}
     $$

3. **[[Subjective Probability]]**:
   - Based on personal judgment or experience.
   - Example: Estimating the chance of rain tomorrow.

---

## Rules of Probability

1. **[[Complement Rule]]**:
   - The probability of the complement of event $A$ is:
     $$
     P(A^c) = 1 - P(A)
     $$

2. **[[Addition Rule]]**:
   - For two events $A$ and $B$:
     $$
     P(A \cup B) = P(A) + P(B) - P(A \cap B)
     $$

3. **[[Multiplication Rule]]**:
   - For independent events:
     $$
     P(A \cap B) = P(A)P(B)
     $$

4. **[[Conditional Probability]]**:
   - The probability of $A$ given $B$:
     $$
     P(A|B) = \frac{P(A \cap B)}{P(B)}, \, \text{if } P(B) > 0
     $$

5. **[[Bayes' Theorem]]**:
   - Updates probabilities based on new evidence:
     $$
     P(A|B) = \frac{P(B|A)P(A)}{P(B)}
     $$

---

## Applications

1. **Machine Learning**:
   - Forms the basis of algorithms like [[Naive Bayes]], [[Hidden Markov Models]], and [[Bayesian Inference]].
2. **[[Risk Analysis]]**:
   - Used in finance and insurance to assess risks.
3. **[[Natural Language Processing|Natural Language Processing (NLP)]]**:
   - Models word probabilities in tasks like [[Language Modeling]].
4. **Decision Making**:
   - Helps optimize strategies in uncertain conditions (e.g., A/B testing).

---

## Common Distributions

1. **Discrete Distributions**:
   - [[Binomial Distribution]]: Probability of successes in a fixed number of trials.
   - [[Poisson Distribution]]: Probability of a given number of events in a fixed interval.

2. **Continuous Distributions**:
   - [[Normal Distribution]]: Symmetric bell-shaped curve.
   - [[Exponential Distribution]]: Time between events in a Poisson process.

---

## Challenges

1. **Uncertainty in Data**:
   - Probabilities are often estimated from incomplete or noisy data.
2. **Dependence vs. Independence**:
   - Many methods assume independence, which may not hold in real-world data.
3. **Rare Events**:
   - Estimating probabilities for rare events requires large datasets or prior knowledge.

---

## Related Topics

- [[Bayes' Theorem]]: Core principle for reasoning under uncertainty.
- [[Conditional Probability]]: Explains relationships between dependent events.
- [[Random Variables]]: Variables that take on values based on random phenomena.
- [[Probability Distributions]]: Describe how probabilities are distributed over outcomes.
- [[Statistics]]: Builds on probability to infer patterns from data.

---

## Aliases
- Probability
- Likelihood Theory

---

## Tags
#probability #mathematics #statistics #machinelearning #inference

---

## Links to Explore
- [[Bayes' Theorem]]: Learn how probability is updated with new evidence.
- [[Conditional Probability]]: Understand dependencies between events.
- [[Random Variables]]: Explore how variables are defined probabilistically.
- [[Probability Distributions]]: Discover key distributions in probability theory.
- [[Statistics]]: Investigate how probability underpins statistical analysis.