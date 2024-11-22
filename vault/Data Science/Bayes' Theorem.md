## Overview
**Bayes' Theorem** is a fundamental concept in [[Probability]] and [[Statistics]] that describes how to update the probability of a hypothesis based on new evidence. It provides a mathematical framework for reasoning under uncertainty and forms the basis of many machine learning algorithms, including [[Naive Bayes]] and [[Bayesian Inference]].

The theorem is expressed as:
$$
P(A|B) = \frac{P(B|A)P(A)}{P(B)}
$$
Where:
- $P(A|B)$: Posterior probability of $A$ given $B$.
- $P(B|A)$: Likelihood of observing $B$ given $A$.
- $P(A)$: Prior probability of $A$.
- $P(B)$: Evidence or marginal probability of $B$.

---

## Key Concepts

1. **Prior Probability ($P(A)$)**:
   - Represents the initial belief about the probability of $A$ before observing any evidence.

2. **Likelihood ($P(B|A)$)**:
   - Measures how well the evidence $B$ supports the hypothesis $A$.

3. **Posterior Probability ($P(A|B)$)**:
   - Updated probability of $A$ after observing evidence $B$.

4. **Evidence ($P(B)$)**:
   - Normalizing constant ensuring probabilities sum to 1. Calculated as:
     $$
     P(B) = \sum_{A} P(B|A)P(A)
     $$

---

## Applications

1. **Machine Learning**:
   - Foundation of [[Naive Bayes]] and other probabilistic models.
2. **Medical Diagnosis**:
   - Compute the probability of a disease given test results.
3. **Spam Detection**:
   - Classify emails as spam or not spam based on word frequencies.
4. **Bayesian Inference**:
   - Update beliefs about model parameters based on observed data.
5. **Decision Making**:
   - Support decision-making under uncertainty in fields like finance and risk management.

---

## Example

### Disease Diagnosis
Suppose:
- $P(Disease) = 0.01$: Prior probability of having the disease.
- $P(Positive|Disease) = 0.95$: Likelihood of testing positive if diseased.
- $P(Positive|No Disease) = 0.05$: Likelihood of testing positive without disease.
- $P(No Disease) = 0.99$: Prior probability of not having the disease.

Using Bayes' Theorem:
$$
P(Disease|Positive) = \frac{P(Positive|Disease)P(Disease)}{P(Positive)}
$$
Where:
$$
P(Positive) = P(Positive|Disease)P(Disease) + P(Positive|No Disease)P(No Disease)
$$
Calculate the posterior probability of having the disease given a positive test result.

---

## Related Topics

- [[Naive Bayes]]: Applies Bayes' Theorem under the assumption of conditional independence.
- [[Bayesian Inference]]: Uses Bayes' Theorem for parameter estimation.
- [[Probability]]: Mathematical foundation for Bayes' Theorem.
- [[Conditional Probability]]: Core concept in understanding Bayes' Theorem.
- [[Likelihood]]: A key term in the theorem's formulation.

---

## Aliases
- Bayes' Theorem
- Bayes Rule
- Bayesian Rule

---

## Tags
#bayestheorem #probability #statistics #machinelearning #inference

---

## Links to Explore
- [[Naive Bayes]]: Learn how Bayes' Theorem is used in classification.
- [[Bayesian Inference]]: Explore parameter estimation using Bayes' Theorem.
- [[Probability]]: Understand the foundational concepts behind Bayes' Theorem.
- [[Conditional Probability]]: Key to applying Bayes' Theorem.
- [[Likelihood]]: Learn about its role in probabilistic models.