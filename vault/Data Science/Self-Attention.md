## Overview
**Self-Attention** is a mechanism used in [[Transformers]] to compute the relationship between different elements (tokens) in a sequence. It allows the model to focus on relevant parts of the input while processing each token, making it essential for tasks like [[Text Generation]], [[Machine Translation]], and [[Summarization]].

---

## Key Concepts

### Definition
Self-attention calculates the importance of each token in a sequence relative to every other token. It assigns a **weight** to each token pair, enabling the model to dynamically attend to relevant information.

### How It Works
Given a sequence of tokens, self-attention computes three vectors for each token:
- **Query $Q$**: Represents the token that is "asking" for information.
- **Key $K$**: Represents the token that contains information to be compared.
- **Value $V$**: Contains the actual information of the token.

The attention score between two tokens is calculated as:
$$
\text{Attention Score} = \frac{Q \cdot K^T}{\sqrt{d_k}}
$$
Where:
- $Q$: Query vector.
- $K^T$: Transposed key vector.
- $d_k$: Dimensionality of the key vector (scaling factor to stabilize gradients).

---

## Steps of Self-Attention

1. **Input Embedding**:
   - Input tokens are embedded into high-dimensional vectors.

2. **Linear Transformations**:
   - Tokens are projected into query (\( Q \)), key (\( K \)), and value (\( V \)) spaces using learned weight matrices.

3. **Attention Scores**:
   - Calculate the similarity between each token's query and every other token's key.

4. **Softmax Normalization**:
   - Convert attention scores into probabilities using the [[Softmax Function]].

5. **Weighted Sum**:
   - Multiply the value (\( V \)) by the attention probabilities to produce the output representation for each token.

---

## Formula

$$
\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V
$$

---

## Multi-Head Self-Attention

### Purpose
- Improves the model's ability to capture different types of relationships between tokens.

### How It Works
- Splits the input into multiple "heads."
- Each head performs self-attention independently, capturing different features.
- Results are concatenated and transformed through a final linear layer.

Formula:
$$
\text{MultiHead}(Q, K, V) = \text{Concat}(\text{head}_1, \dots, \text{head}_h)W^O
$$

---

## Applications

1. **[[Natural Language Processing]]**:
   - Captures contextual relationships between words in a sentence.
   - Used in tasks like [[Named Entity Recognition (NER)]] and [[Question Answering]].

2. **[[Machine Translation]]**:
   - Aligns tokens in the source language with their counterparts in the target language.

3. **[[Text Summarization]]**:
   - Identifies the most important sentences or words in a document.

4. **[[Computer Vision]]**:
   - Adapted in Vision Transformers (ViT) to model relationships between image patches.

---

## Advantages

1. **Captures Long-Range Dependencies**:
   - Models relationships across tokens, regardless of their distance in the sequence.

2. **Parallelizable**:
   - Unlike [[Recurrent Neural Networks (RNNs)]], self-attention processes tokens simultaneously, speeding up computation.

3. **Dynamic Focus**:
   - Adjusts attention weights based on the input, making it adaptable to different contexts.

---

## Disadvantages

1. **Quadratic Complexity**:
   - Requires $O(n^2)$ operations, where $n$ is the sequence length, making it memory-intensive for long sequences.

2. **Limited Context Window**:
   - Restricted by the model's maximum sequence length, often requiring truncation for very long inputs.

---

## Alternatives and Enhancements

1. **[[Relative Positional Encoding]]**:
   - Improves self-attention by incorporating relative distances between tokens.

2. **[[Sparse Attention]]**:
   - Reduces computational complexity by focusing only on a subset of tokens.

3. **[[Efficient Transformers]]**:
   - Models like [[Performer]] or [[Linformer]] reduce the $O(n^2)$ complexity to linear time.

---

## Tools and Libraries

1. **TensorFlow**:
   - Includes built-in layers for self-attention in `tf.keras.layers.Attention`.
2. **PyTorch**:
   - Provides tools for implementing custom attention layers or using pre-trained models.
3. **Hugging Face Transformers**:
   - Implements self-attention in pre-trained Transformer models.

---

## Related Topics
- [[Transformers]]: Core architecture leveraging self-attention.
- [[Multi-Head Attention]]: Extends self-attention for better feature extraction.
- [[Positional Encoding]]: Injects sequence order information into self-attention.
- [[BERT]]: Uses self-attention for bidirectional encoding.

---

## Resources

### Research Papers
- *[[Attention Is All You Need]]* (Vaswani et al., 2017): Introduced the self-attention mechanism.

### Tutorials
- TensorFlow: Implementing self-attention layers.
- PyTorch: Custom self-attention in sequence models.

### Books
- *Deep Learning* by Ian Goodfellow, Yoshua Bengio, and Aaron Courville.
- *Speech and Language Processing* by Jurafsky and Martin.

---

## Tags
#selfattention #transformers #machinelearning #NLP #sequence-modeling