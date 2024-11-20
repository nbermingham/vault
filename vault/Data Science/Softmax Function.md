## Overview
The **Softmax Function** is a mathematical function that converts a vector of real numbers into a probability distribution. It is widely used in [[Machine Learning]] models, particularly for multi-class [[Classification]] tasks and in attention mechanisms like [[Self-Attention]] within [[Transformers]]. 

---

## Key Concepts

### Definition
The Softmax function maps a vector $z = [z_1, z_2, \dots, z_n]$ into a probability distribution $\sigma(z)$, where:
$$
\sigma(z_i) = \frac{\exp(z_i)}{\sum_{j=1}^n \exp(z_j)}
$$
Where:
- $z_i$: Input element.
- $n$: Number of elements in the input vector.
- $\exp$: [[Exponential function]].

### Properties
1. **Output Range**:
   - Values are in the range \( (0, 1) \), making them interpretable as probabilities.
2. **Sum-to-One**:
   - The sum of the output probabilities is always \( 1 \):
     $$
     \sum_{i=1}^n \sigma(z_i) = 1
     $$
3. **Exponentially Scaled**:
   - Larger values of $z_i$ dominate the output distribution due to the exponential function.

---

## Applications

### 1. [[Multi-Class Classification]]
- Used in the output layer of models to predict probabilities for each class.
- Example: In a neural network for image [[Classification]], the Softmax function converts logits (raw outputs) into class probabilities.

### 2. [[Attention Mechanism]]
- In [[Self-Attention]], Softmax normalizes attention scores across all tokens in a sequence:
  $$
  \text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V
  $$

### 3. Reinforcement Learning
- Converts action preferences into a probability distribution for decision-making.

---

## Mathematical Properties

### Gradient
The derivative of the Softmax function with respect to \( z_i \) is:
$$
\frac{\partial \sigma(z_i)}{\partial z_j} =
\begin{cases}
\sigma(z_i) \cdot (1 - \sigma(z_i)), & \text{if } i = j \\
-\sigma(z_i) \cdot \sigma(z_j), & \text{if } i \neq j
\end{cases}
$$

### Log-Softmax
The log of the Softmax function is often used to simplify computations in loss functions like [[Cross-Entropy Loss]]:
$$
\log \sigma(z_i) = z_i - \log \left( \sum_{j=1}^n \exp(z_j) \right)
$$

---

## Advantages

1. **Interpretable Outputs**:
   - Converts model outputs into probabilities that are easy to interpret.
2. **Normalization**:
   - Ensures outputs are normalized, making them suitable for probabilistic models.
3. **Differentiable**:
   - Fully differentiable, enabling backpropagation in neural networks.

---

## Disadvantages

1. **Numerical Instability**:
   - Exponentials can lead to large values, causing overflow. 
   - **Solution**: Subtract the maximum value from the input vector before applying Softmax:
     $$
     \sigma(z_i) = \frac{\exp(z_i - \max(z))}{\sum_{j=1}^n \exp(z_j - \max(z))}
     $$

2. **Non-Sparse Outputs**:
   - Produces non-zero probabilities for all classes, which may not be ideal in some cases.

---

## Tools and Libraries

1. **TensorFlow**:
   - `tf.nn.softmax`: Computes the Softmax function.
2. **PyTorch**:
   - `torch.nn.functional.softmax`: Applies the Softmax function to tensors.
3. **NumPy**:
   - Can implement Softmax manually using `np.exp`.

---

## Example

### Input Vector
$$
z = [2.0, 1.0, 0.1]
$$

### Applying Softmax
$$
\sigma(z_1) = \frac{\exp(2.0)}{\exp(2.0) + \exp(1.0) + \exp(0.1)} = 0.659
$$
$$
\sigma(z_2) = \frac{\exp(1.0)}{\exp(2.0) + \exp(1.0) + \exp(0.1)} = 0.242
$$
$$
\sigma(z_3) = \frac{\exp(0.1)}{\exp(2.0) + \exp(1.0) + \exp(0.1)} = 0.099
$$

Output:
$$
\sigma(z) = [0.659, 0.242, 0.099]
$$

---

## Related Topics
- [[Cross-Entropy Loss]]: Often paired with Softmax for [[Classification]] tasks.
- [[Logistic Regression]]: A binary [[Classification]] algorithm where Softmax can generalize to multi-class settings.
- [[Self-Attention]]: Uses Softmax to normalize attention scores in Transformers.

---

## Resources

### Tutorials
- TensorFlow: Softmax activation in [[Classification]] tasks.
- PyTorch: Using Softmax for multi-class classification.

### Books
- *Deep Learning* by Ian Goodfellow, Yoshua Bengio, and Aaron Courville.
- *Hands-On Machine Learning with [[Scikit-learn]], Keras, and TensorFlow* by Aurélien Géron.

---

## Tags
#softmax #machinelearning #deep-learning #[[Classification]] #selfattention