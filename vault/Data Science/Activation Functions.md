## Overview
**Activation Functions** are mathematical functions applied to the outputs of [[Neural Networks]] at each layer. They introduce non-linearity into the network, allowing it to model complex patterns and solve problems beyond simple linear relationships. Without activation functions, a neural network would behave like a linear model, regardless of its depth.

Activation functions play a crucial role in determining the network's performance and convergence during [[Gradient Descent]] optimization.

---

## Types of Activation Functions

### 1. **[[Linear Activation]]**
$$
f(x) = x
$$
- **Usage**: Rarely used in modern networks since it does not introduce non-linearity.
- **Disadvantage**: Prevents the network from learning complex patterns.

---

### 2. **[[Sigmoid Function]]**
$$
f(x) = \frac{1}{1 + e^{-x}}
$$
- **Output Range**: $(0, 1)$.
- **Usage**: Historically used in the output layer for binary classification.
- **Issues**:
  - **Vanishing Gradients**: [[Gradients]] approach zero for large or small inputs.
  - **Non-Zero Mean**: Can slow convergence.

---

### 3. **Hyperbolic Tangent ([[Tanh]])**
$$
f(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}
$$
- **Output Range**: $(-1, 1)$.
- **Usage**: Improves over sigmoid by centering outputs around zero.
- **Issues**:
  - Suffers from the **[[Vanishing Gradient Problem]]** for large inputs.

---

### 4. **[[ReLU]] (Rectified Linear Unit)**
$$
f(x) = \max(0, x)
$$
- **Output Range**: $[0, \infty)$.
- **Usage**: Widely used in modern deep networks due to simplicity and efficiency.
- **Advantages**:
  - Computationally efficient.
  - Reduces vanishing gradient issues.
- **Issues**:
  - **Dead Neurons**: Nodes can "die" if gradients become zero permanently.

---

### 5. **[[Leaky ReLU]]**
$$
f(x) = \begin{cases} 
x & x > 0 \\
\alpha x & x \leq 0
\end{cases}
$$
- **Output Range**: $(-\infty, \infty)$.
- **Usage**: Addresses the "dead neuron" problem in ReLU.
- **Parameter**: $\alpha$ controls the slope for negative inputs.

---

### 6. **[[Softmax Function]]**
$$
f(x_i) = \frac{e^{x_i}}{\sum_{j=1}^n e^{x_j}}
$$
- **Output Range**: $(0, 1)$ for each class.
- **Usage**: Commonly used in the output layer for multi-class classification tasks.
- **Purpose**: Converts raw scores into probabilities.

---

### 7. **[[Swish]]**
$$
f(x) = x \cdot \text{sigmoid}(x)
$$
- **Usage**: Offers smooth gradients and improves training in deeper networks.
- **Advantages**:
  - Does not "saturate" like sigmoid or tanh.
  - Retains non-linearity.

---

## Key Properties of Activation Functions

1. **Non-Linearity**:
   - Enables the network to approximate complex functions.
2. **[[Differentiability]]**:
   - Essential for optimization with [[Backpropagation]].
3. **Range**:
   - Impacts the flow of gradients and convergence during training.
4. **Efficiency**:
   - Functions like ReLU are computationally efficient and widely used.

---

## Comparison Table

| Activation Function   | Output Range      | Non-Linearity | Gradient Issues            | Common Applications        |
|------------------------|-------------------|---------------|----------------------------|----------------------------|
| Linear                | $(-\infty, \infty)$ | No            | No gradient vanishing      | Rarely used               |
| Sigmoid               | $(0, 1)$          | Yes           | Vanishing gradients        | Binary classification     |
| Tanh                  | $(-1, 1)$         | Yes           | Vanishing gradients        | RNNs, regression          |
| ReLU                  | $[0, \infty)$     | Yes           | Dead neurons               | Deep networks             |
| Leaky ReLU            | $(-\infty, \infty)$ | Yes          | Rare dead neurons          | Deep networks             |
| Softmax               | $(0, 1)$          | Yes           | None                       | Multi-class classification |
| Swish                 | $(-\infty, \infty)$ | Yes          | None                       | Deep networks             |

---

## Applications

1. **Regression**:
   - Use linear activation for output layers.
2. **Binary Classification**:
   - Use sigmoid activation in the output layer.
3. **Multi-Class Classification**:
   - Use softmax in the output layer.
4. **Hidden Layers**:
   - ReLU and its variants (Leaky ReLU, Swish) are widely used in hidden layers.

---

## Related Topics

- [[Neural Networks]]: Activation functions are a core component of network layers.
- [[Backpropagation]]: Requires differentiable activation functions for computing gradients.
- [[Gradient Descent]]: Optimization relies on gradients influenced by activation functions.
- [[Softmax Function]]: Commonly used for probability-based outputs in classification tasks.
- [[ReLU]]: The most widely used activation function in modern deep learning.

---

## Tags
#activation-functions #neural-networks #deep-learning #machinelearning #optimization