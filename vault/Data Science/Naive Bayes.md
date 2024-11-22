## Overview
**Naive Bayes** is a family of simple yet powerful probabilistic [[Classification]] algorithms based on applying Bayes' Theorem. It assumes that the features are conditionally independent, which simplifies computation and makes it "naive." Despite this simplifying assumption, Naive Bayes performs well in many real-world applications, especially in text classification and [[Natural Language Processing (NLP)]] tasks.

---

## Key Concepts

1. **Bayes' Theorem**:
   - The foundation of Naive Bayes:
     $$
     P(C|X) = \frac{P(X|C)P(C)}{P(X)}
     $$
     Where:
     - $P(C|X)$: Posterior probability of class $C$ given features $X$.
     - $P(X|C)$: Likelihood of features $X$ given class $C$.
     - $P(C)$: Prior probability of class $C$.
     - $P(X)$: Evidence or marginal probability of features $X$.

2. **Conditional Independence Assumption**:
   - Assumes that all features are independent given the class label:
     $$
     P(X|C) = \prod_{i=1}^n P(x_i|C)
     $$
     Where $x_i$ is the $i$-th feature in the feature vector $X$.

3. **Classification Rule**:
   - Predict the class $C$ that maximizes the posterior probability:
     $$
     C = \arg\max_{C_k} P(C_k) \prod_{i=1}^n P(x_i|C_k)
     $$

---

## Variants of Naive Bayes

1. **[[Gaussian Naive Bayes]]**:
   - Assumes continuous features follow a Gaussian (normal) distribution.
   - Used in tasks with numeric features.

2. **[[Multinomial Naive Bayes]]**:
   - Suitable for discrete features like word counts in [[Text Classification]].
   - Often used for document classification and spam detection.

3. **[[Bernoulli Naive Bayes]]**:
   - Assumes binary features (presence or absence of features).
   - Commonly applied in [[Sentiment Analysis]] or binary classification tasks.

---

## Applications

1. **Text Classification**:
   - Spam detection, news categorization, and sentiment analysis.
2. **Recommendation Systems**:
   - Predict user preferences based on past behavior.
3. **Medical Diagnosis**:
   - Classify diseases based on symptoms and test results.
4. **Real-Time Prediction**:
   - Used in applications requiring quick classification due to its computational efficiency.

---

## Advantages

1. **Simplicity**:
   - Easy to implement and computationally efficient.
2. **Handles High-Dimensional Data**:
   - Performs well with sparse and high-dimensional datasets, such as text data.
3. **Robustness**:
   - Works well even when the independence assumption is violated to some extent.

---

## Disadvantages

1. **Independence Assumption**:
   - The naive assumption of feature independence is rarely true in real-world data.
2. **[[Zero Probability Problem]]**:
   - If a feature never occurs with a class in training data, it assigns zero probability to that class.
     - **Solution**: Use techniques like Laplace smoothing.
3. **Limited Expressiveness**:
   - Naive Bayes is not suitable for tasks where feature interactions are critical.

---

## Example

### Multinomial Naive Bayes
Given:
- Two classes: Spam and Not Spam.
- Features: Word counts for "buy," "free," and "hello."

Calculate:
1. [[Priors]]: $P(Spam)$, $P(Not Spam)$.
2. [[Likelihoods]]: $P(word|Spam)$ and $P(word|Not Spam)$.
3. [[Posterior]]: Multiply prior and likelihood for each class and predict the class with the higher posterior probability.

---

## Related Topics

- [[Bayes' Theorem]]: Foundation of Naive Bayes.
- [[Text Classification]]: A common application of Naive Bayes.
- [[Sentiment Analysis]]: Often implemented using Naive Bayes.
- [[Multinomial Naive Bayes]]: Specialization for text data.
- [[Probability]]: Core mathematical foundation for Naive Bayes.

---

## Aliases
- Naive Bayes
- Naive Bayes Classifier

---

## Tags
#naivebayes #classification #machinelearning #textclassification #probability

---

## Links to Explore
- [[Bayes' Theorem]]: Understand the mathematical basis of Naive Bayes.
- [[Text Classification]]: Discover how Naive Bayes is applied to text data.
- [[Multinomial Naive Bayes]]: Explore its use in NLP tasks.
- [[Sentiment Analysis]]: Learn how Naive Bayes handles binary text classification.
- [[Probability]]: Understand the probabilistic principles behind Naive Bayes.