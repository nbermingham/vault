## Overview
**Full Attention** is the standard implementation of the [[Attention Mechanism]] in transformer-based models like [[BERT]] and [[GPT]]. It computes pairwise attention scores for all tokens in the input sequence, resulting in an attention matrix of size $n \times n$, where $n$ is the sequence length.

Full Attention is highly effective at capturing global relationships between all tokens in a sequence, but its quadratic complexity ($O(n^2)$) in memory and computation can make it inefficient for processing long sequences.

---

## Key Concepts

### **1. Attention Mechanism**
- Full Attention allows each token to attend to every other token in the input sequence.
- The attention scores are computed using:
  $$
  \text{Attention}(Q, K, V) = \text{Softmax}\left(\frac{QK^\top}{\sqrt{d_k}}\right)V
  $$
  Where:
  - $Q$: Query matrix.
  - $K$: Key matrix.
  - $V$: Value matrix.
  - $d_k$: Dimensionality of keys/queries.

### **2. Attention Matrix**
- The attention matrix has dimensions $n \times n$, where $n$ is the sequence length.
- Each element represents the attention weight between two tokens, allowing for complete connectivity across the sequence.

### **3. Quadratic Complexity**
- Memory and computation grow quadratically with sequence length:
  - $O(n^2)$ for storing the attention matrix.
  - $O(n^2d)$ for computing attention scores, where $d$ is the dimensionality of the embeddings.

---

## Advantages

1. **Global Context**:
   - Full Attention captures relationships between all tokens in a sequence, making it highly effective for tasks like [[Machine Translation]] and [[Text Generation]].

2. **Flexibility**:
   - Works well across various tasks and domains without requiring custom patterns or assumptions about token relationships.

3. **Accuracy**:
   - Often achieves higher accuracy compared to sparse or approximate attention mechanisms.

---

## Disadvantages

1. **Computational Cost**:
   - Full Attention is computationally expensive for long sequences, limiting its scalability in tasks like [[Document Classification]] or [[Speech Recognition]].

2. **Memory Usage**:
   - Storing the $n \times n$ attention matrix can become prohibitive for large sequences or datasets.

3. **Redundancy**:
   - For very long sequences, not all token relationships are equally important, leading to wasted computation on irrelevant pairs.

---

## Techniques to Address Limitations

1. **Sparse Attention**:
   - Reduces computation by attending only to a subset of token pairs (e.g., [[Longformer]], [[BigBird]]).
2. **Linear Attention**:
   - Approximates Full Attention with linear complexity ($O(n)$), making it more scalable.
3. **Efficient Transformers**:
   - Explore various methods like [[Performer]] and [[Reformer]] to optimize attention mechanisms.

---

## Applications

1. **Natural Language Processing (NLP)**:
   - [[Text Classification]], [[Machine Translation]], [[Named Entity Recognition]].
2. **Vision Transformers (ViT)**:
   - Adapts Full Attention for [[Image Classification]] by flattening image patches.
3. **Generative Models**:
   - Used in [[GPT]] for tasks like text generation and summarization.

---

## Comparison with Sparse Attention

| Feature               | Full Attention                     | Sparse Attention                   |
|-----------------------|-------------------------------------|-------------------------------------|
| **Complexity**        | $O(n^2)$                           | $O(n \cdot k)$                     |
| **Memory Usage**      | High                               | Reduced                            |
| **Global Relationships** | Captures all                    | May miss some                      |
| **Scalability**       | Limited                            | High                               |
| **Accuracy**          | Typically higher                   | Slightly lower for some tasks      |

---

## Related Topics

- [[Attention Mechanism]]: The broader concept behind Full Attention.
- [[Sparse Attention]]: An efficient alternative for long sequences.
- [[Transformers]]: Full Attention is a core operation in transformer models.
- [[Self-Attention]]: Full Attention is the default implementation of Self-Attention.
- [[Efficient Transformers]]: Techniques to optimize the attention mechanism.

---

## Aliases
- Full Attention
- Quadratic Attention
- Full Self-Attention
- Standard Attention
- Dense Attention

---

## Tags
#full-attention #attention-mechanism #transformers #self-attention #deep-learning #NLP

---

## Links to Explore
- [[Attention Mechanism]]: Learn the foundational concept behind Full Attention.
- [[Transformers]]: Understand how Full Attention operates in these architectures.
- [[Sparse Attention]]: Explore alternatives to Full Attention for long sequences.
- [[Self-Attention]]: Dive deeper into how Full Attention