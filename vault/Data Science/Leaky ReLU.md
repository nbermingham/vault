## Overview
**Leaky ReLU (Rectified Linear Unit)** is a variation of the [[ReLU]] activation function used in [[Neural Networks]] and [[Deep Learning]] to address the issue of "dead neurons." Unlike [[ReLU]], which outputs zero for all negative inputs, Leaky ReLU allows a small, non-zero gradient for negative inputs, making it less likely for neurons to become inactive during training.

Leaky ReLU introduces a small slope $\alpha$ for negative values, ensuring gradients flow even when the input is less than zero.

---

## Formula
The Leaky ReLU activation function is defined as:
$$
f(x) = 
\begin{cases} 
x & \text{if } x > 0, \\
\alpha x & \text{if } x \leq 0,
\end{cases}
$$
Where:
- $\alpha$: A small positive constant (e.g., $0.01$) that determines the slope for negative inputs.
- $x$: The input value.

---

## Key Concepts

1. **Small Slope for Negative Inputs**:
   - The parameter $\alpha$ allows a small amount of negative input to pass through, ensuring gradients are not zero.

2. **Non-Linearity**:
   - Like other [[Activation Functions]], Leaky ReLU introduces non-linearity into the network, enabling the modeling of complex patterns.

3. **Avoids Dead Neurons**:
   - In [[ReLU]], neurons can "die" if their gradients become zero permanently. Leaky ReLU reduces this risk by maintaining a small gradient for negative inputs.

---

## Advantages

1. **Prevents Dead Neurons**:
   - Unlike [[ReLU]], Leaky ReLU allows gradients to flow for negative inputs, reducing the likelihood of neurons becoming inactive.

2. **Efficient Computation**:
   - Simple to implement and computationally efficient, similar to [[ReLU]].

3. **Smooth Training**:
   - Ensures continuous learning by providing non-zero gradients across all input ranges.

---

## Disadvantages

1. **Hyperparameter Sensitivity**:
   - Requires tuning of the $\alpha$ parameter, which can affect model performance.

2. **Less Popular in Practice**:
   - Variants like [[Parametric ReLU (PReLU)]] and [[Swish]] are sometimes preferred for improved flexibility or performance.

---

## Applications

1. **[[Deep Neural Networks]]**:
   - Commonly used in hidden layers to improve gradient flow during training.

2. **Avoiding Vanishing Gradients**:
   - Leaky ReLU is often chosen for deep architectures where the [[Vanishing Gradient Problem]] is a concern.

3. **Image Processing**:
   - Frequently used in [[Convolutional Neural Networks (CNNs)]] for tasks like [[Image Classification]] and [[Object Detection]].

---

## Variants

1. **[[ReLU]]**:
   - Outputs zero for all negative inputs, potentially causing dead neurons.

2. **[[Parametric ReLU (PReLU)]]**:
   - Similar to Leaky ReLU but learns the slope $\alpha$ during training.

3. **[[Swish]]**:
   - A smoother activation function offering better gradients and performance.

---

## Related Topics

- [[Activation Functions]]: Leaky ReLU is one of many non-linear activation functions used in neural networks.
- [[ReLU]]: The most commonly used activation function, from which Leaky ReLU is derived.
- [[Parametric ReLU (PReLU)]]: A learnable variation of Leaky ReLU.
- [[Vanishing Gradient Problem]]: Leaky ReLU addresses this issue by maintaining gradients for negative inputs.
- [[Convolutional Neural Networks (CNNs)]]: Often use Leaky ReLU in hidden layers for better feature extraction.

---

## Aliases
- Leaky ReLU
- Leaky Rectified Linear Unit
- LReLU
- Modified ReLU
- Non-Zero ReLU

---

## Tags
#leaky-relu #activation-functions #neural-networks #deeplearning #gradient-flow