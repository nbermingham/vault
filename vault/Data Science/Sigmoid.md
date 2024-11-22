## Overview
The **Sigmoid Function** is a commonly used [[Activation Functions|Activation Function]] in [[Neural Networks]] that maps any real-valued input to a value between 0 and 1. This makes it particularly useful for tasks where outputs need to represent probabilities, such as [[Logistic Regression]] and binary classification problems.
![[Pasted image 20241121103103.png]]

The function is defined as:
$$
\sigma(x) = \frac{1}{1 + e^{-x}}
$$
Where:
- $x$: Input to the function.
- $\sigma(x)$: Output, bounded between 0 and 1.

---

## Key Characteristics

1. **S-shaped Curve**:
   - The sigmoid function has an "S" shape, smoothly transitioning from 0 to 1.
2. **Output Range**:
   - The function outputs values between 0 and 1, making it ideal for probability representation.
3. **Monotonic**:
   - The function is strictly increasing, ensuring that larger inputs always yield larger outputs.

---

## Applications

1. **Binary Classification**:
   - Converts raw model outputs (logits) into probabilities for classes 0 and 1.
2. **Logistic Regression**:
   - Used as the activation function in [[Logistic Regression]] to model probabilities.
3. **Hidden Layers** (historically):
   - Previously used in the hidden layers of shallow neural networks, though now largely replaced by [[ReLU]] for better performance.

---

## Advantages

1. **Probability Output**:
   - Naturally produces outputs in the range [0, 1], making it interpretable as probabilities.
2. **Smooth Gradient**:
   - The sigmoid function is differentiable, which is useful for [[Backpropagation]].

---

## Disadvantages

1. **Vanishing Gradient Problem**:
   - Gradients become very small for extreme input values, slowing down training in deep networks.
   - Example: For $|x| \gg 0$, $\sigma'(x)$ approaches 0, leading to tiny weight updates.
2. **Non-Zero Centered Output**:
   - Outputs are always positive, leading to less efficient optimization during [[Gradient Descent]].
3. **Saturation**:
   - For large positive or negative inputs, the function saturates, yielding gradients close to zero.

---

## Comparison with Other Activation Functions

| Feature               | Sigmoid                       | [[ReLU]]                     | [[Tanh]]                     |
|-----------------------|-------------------------------|------------------------------|------------------------------|
| **Range**             | (0, 1)                       | [0, $\infty$)               | (-1, 1)                     |
| **Vanishing Gradient**| Yes                           | No                           | Yes                          |
| **Zero-Centered**     | No                            | No                           | Yes                          |
| **Computational Cost**| High                         | Low                          | Moderate                     |

---

## Example Workflow

1. **Logistic Regression**:
   - Apply sigmoid to compute probabilities:
     $$
     P(y=1 \mid x) = \frac{1}{1 + e^{-z}}
     $$
   - Where $z = w \cdot x + b$ is the linear transformation of inputs.

2. **Neural Network Output Layer**:
   - Use sigmoid activation for binary classification problems.

---

## Related Topics

- [[Activation Function]]: Sigmoid is one of the classic activation functions in neural networks.
- [[Vanishing Gradient Problem]]: A challenge often associated with sigmoid in deep networks.
- [[Logistic Regression]]: A common application of the sigmoid function.
- [[Tanh]]: A related activation function with outputs in the range (-1, 1).
- [[ReLU]]: A more modern activation function that overcomes some limitations of sigmoid.

---

## Aliases
- Sigmoid
- Logistic Function
- Sigmoid Activation Function

---

## Tags
#sigmoid #activationfunction #machinelearning #neuralnetworks #logisticregression

---

## Links to Explore
- [[Activation Function]]: Understand the role of activation functions in neural networks.
- [[Vanishing Gradient Problem]]: Explore challenges faced by sigmoid in deep learning.
- [[Logistic Regression]]: Learn about the core application of the sigmoid function.
- [[Tanh]]: Discover an alternative activation function with similar characteristics.
- [[ReLU]]: Compare sigmoid with this widely used activation function.