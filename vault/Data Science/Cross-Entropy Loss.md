# Cross-Entropy Loss

## Overview
**Cross-Entropy Loss** is a widely used loss function in [[Machine Learning]] and [[Deep Learning]], especially for classification tasks. It measures the difference between two probability distributions: the predicted probability distribution from the model and the true labels (encoded as one-hot vectors).

Cross-Entropy Loss is often used in conjunction with the [[Softmax Function]] for multi-class classification tasks.

---

## Key Concepts

### Definition
Cross-Entropy Loss quantifies the distance between the predicted probabilities $\hat{y}$ and the true labels $y$. For a single sample:
$$
L = - \sum_{i=1}^C y_i \log(\hat{y}_i)
$$
Where:
- $C$: Number of classes.
- $y_i$: True label for class $i$ (1 if the class is correct, 0 otherwise).
- $\hat{y}_i$: Predicted probability for class $i$ (output of the [[Softmax Function]]).

### Intuition
- Cross-Entropy Loss penalizes incorrect predictions with high confidence more heavily than less confident ones.
- When the predicted probability for the correct class is high, the loss is small.
- When the predicted probability for the correct class is low, the loss is large.

---

## Relationship to [[Kullback-Leibler Divergence]]

Cross-Entropy Loss can be interpreted as the sum of the [[Kullback-Leibler Divergence]] (KL Divergence) between the true distribution $P$ and the predicted distribution $Q$, plus the entropy of $P$. 

### KL Divergence Interpretation
KL Divergence quantifies how much information is lost when the predicted distribution approximates the true distribution. It is defined as:
$$
D_{KL}(P || Q) = \sum_{i=1}^C P(x_i) \log\left(\frac{P(x_i)}{Q(x_i)}\right)
$$

For classification tasks:
- $P$ is the true distribution, often represented as a one-hot vector.
- $Q$ is the predicted probability distribution from the model.

### Cross-Entropy and KL Divergence
The Cross-Entropy Loss can be written as:
$$
H(P, Q) = H(P) + D_{KL}(P || Q)
$$
Where:
- $H(P, Q)$: Cross-Entropy Loss.
- $H(P)$: Entropy of the true distribution.
- $D_{KL}(P || Q)$: KL Divergence between $P$ and $Q$.

Since $H(P)$ is constant during training, minimizing Cross-Entropy Loss is equivalent to minimizing KL Divergence.

---

## Variants

### [[Binary Cross-Entropy Loss]]
For binary classification tasks:
$$
L = - \left[ y \log(\hat{y}) + (1 - y) \log(1 - \hat{y}) \right]
$$
Where:
- $y$: True binary label $0$ or $1$.
- $\hat{y}$: Predicted probability for the positive class.

### [[Categorical Cross-Entropy Loss]]
Used for multi-class classification:
$$
L = - \sum_{i=1}^C y_i \log(\hat{y}_i)
$$
Where:
- $y_i$ is one-hot encoded, with 1 for the correct class and 0 otherwise.

---

## Applications

1. **[[Classification]]**:
   - **[[Binary Classification]]**:
     - Example: Spam detection.
   - **Multi-Class Classification**:
     - Example: Image classification across multiple categories.
2. **[[Language Modeling]]**:
   - Used to optimize models like [[GPT]] and [[BERT]].
3. **[[Reinforcement Learning]]**:
   - Cross-entropy is used to measure policy performance in some algorithms.

---

## Advantages

1. **Probabilistic Interpretability**:
   - Measures the divergence between predicted probabilities and true labels.
2. **Sensitivity to Incorrect Predictions**:
   - Penalizes confident wrong predictions more heavily, encouraging accurate models.
3. **Works Well with Softmax**:
   - Cross-Entropy Loss naturally complements the [[Softmax Function]] in multi-class settings.

---

## Disadvantages

1. **Numerical Instability**:
   - Logarithms of small predicted probabilities can lead to numerical issues.
   - **Solution**: Use a stabilized implementation that adds a small constant ($\epsilon$) to prevent $\log(0)$.
2. **[[Class Imbalance]]**:
   - Performs poorly on datasets with imbalanced classes unless weights or resampling techniques are applied.

---

## Example

### Multi-Class Example
Consider a classification task with 3 classes:
- True label ($y$): [0, 1, 0] (Class 2 is correct).
- Predicted probabilities ($\hat{y}$): [0.1, 0.7, 0.2].

Cross-Entropy Loss:
$$
L = - \left[ 0 \cdot \log(0.1) + 1 \cdot \log(0.7) + 0 \cdot \log(0.2) \right] = -\log(0.7) \approx 0.357
$$

---

## Related Topics
- [[Softmax Function]]: Used to convert logits into probabilities before applying Cross-Entropy Loss.
- [[Logistic Regression]]: Uses Binary Cross-Entropy Loss for binary classification.
- [[Classification Metrics]]: Metrics like accuracy and F1-score complement Cross-Entropy Loss.
- [[Kullback-Leibler Divergence]]: Related to Cross-Entropy in measuring distribution differences.
- [[Entropy]]: A foundational concept underlying Cross-Entropy.

---

## Resources

### Research Papers
- *A Probabilistic Theory of Pattern Recognition* by Devroye et al. (2001): Discusses Cross-Entropy in classification.
- *Deep Learning* by Goodfellow et al.: Explains Cross-Entropy in optimization contexts.

### Tutorials
- TensorFlow and PyTorch official documentation on loss functions.
- Online courses like Coursera's *Deep Learning Specialization*.

### Books
- *Deep Learning* by Ian Goodfellow, Yoshua Bengio, and Aaron Courville.
- *Hands-On Machine Learning with [[Scikit-learn]], Keras, and TensorFlow* by Aurélien Géron.

---

## Tags
#cross-entropy-loss #classification #machinelearning #NLP #softmax #kl-divergence