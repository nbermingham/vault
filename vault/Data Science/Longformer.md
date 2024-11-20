## Overview
**Longformer** is a transformer-based model designed to handle long sequences efficiently by replacing the traditional [[Full Attention]] mechanism with a combination of **Sparse Attention** patterns. It achieves linear complexity, $O(n)$, as opposed to the quadratic complexity, $O(n^2)$, of standard [[Transformers]], making it ideal for tasks involving long documents or sequences.

Developed by AllenAI, Longformer introduces **sliding window attention** and optional global attention to focus on relevant parts of the input while preserving computational and memory efficiency.

---

## Key Concepts

### **1. Sparse Attention**
- Longformer employs **Sparse Attention** to reduce computational complexity:
  - **Sliding Window Attention**:
    - Attends to local neighborhoods (e.g., a fixed number of nearby tokens for each token).
  - **Global Attention**:
    - Allows specific tokens, like [CLS] or query-related tokens, to attend to all tokens in the sequence.
  - **Dilated Attention** (optional):
    - Expands the attention span by skipping over tokens at regular intervals, enabling broader context capture.

### **2. Attention Complexity**
- Standard [[Self-Attention]] computes attention for all token pairs, resulting in $O(n^2)$ complexity.
- Longformer reduces this to $O(n \cdot w)$, where $w$ is the window size for sliding window attention, making it scalable for sequences up to tens of thousands of tokens.

### **3. Hybrid Attention Patterns**
- Combines local and global attention to balance efficiency with performance:
  - Local tokens attend only to nearby tokens (capturing local context).
  - Global tokens attend to all tokens (capturing global context).
  - Example: In [[Document Classification]], the [CLS] token can have global attention, while other tokens use sliding window attention.

---

## Applications

1. **Document Classification**:
   - Processes long documents without truncation, preserving important context for tasks like legal text analysis and scientific paper classification.

2. **Text Summarization**:
   - Summarizes lengthy articles by efficiently attending to relevant parts.

3. **Question Answering**:
   - Longformer excels in tasks requiring context across large passages (e.g., open-domain QA).

4. **Natural Language Understanding (NLU)**:
   - Handles large contexts in tasks like coreference resolution and discourse analysis.

---

## Advantages

1. **Scalability**:
   - Linear complexity allows handling sequences that would be infeasible with traditional [[Transformers]].

2. **Flexibility**:
   - Configurable attention patterns (sliding window, global) make it adaptable to various tasks.

3. **Preserves Context**:
   - Processes entire sequences without truncation, retaining critical information for downstream tasks.

---

## Disadvantages

1. **Limited Global Context**:
   - Sparse patterns may miss some global dependencies unless explicitly configured with global attention.

2. **Complexity in Configuration**:
   - Requires careful design of attention patterns (e.g., determining which tokens should use global attention).

3. **Hardware Dependence**:
   - Requires GPU/TPU acceleration for optimal performance on large sequences.

---

## Comparison with Other Models

| Feature                  | Longformer                      | [[BERT]]                          | [[BigBird]]                       |
|--------------------------|----------------------------------|------------------------------------|------------------------------------|
| **Attention Mechanism**  | Sparse (sliding + global)       | Full                              | Sparse (local + global + random)  |
| **Complexity**           | $O(n)$                          | $O(n^2)$                          | $O(n)$                            |
| **Max Sequence Length**  | 16,384 tokens                   | 512 tokens                        | 16,384 tokens                     |
| **Primary Use Case**     | Long documents                  | Short sequences                   | Long sequences                    |

---

## Tools and Frameworks

1. **Hugging Face Transformers**:
   - Longformer is implemented in the Hugging Face library (`transformers`), making it accessible for practical use.
   - Example models: `allenai/longformer-base-4096`, `allenai/longformer-large-4096`.

2. **PyTorch and TensorFlow**:
   - Custom implementations can be built using Sparse Attention patterns.

---

## Example Workflow

1. **Preprocessing**:
   - Tokenize text into long sequences using a Longformer tokenizer.
   - Designate tokens for global attention (e.g., [CLS], [SEP], or question tokens).
2. **Model Initialization**:
   - Load pre-trained Longformer models or fine-tune on specific tasks.
3. **Training/Inference**:
   - Use sliding window attention for local dependencies and global attention for task-relevant tokens.

---

## Related Topics

- [[Sparse Attention]]: Longformer relies on this mechanism to achieve linear complexity.
- [[Transformers]]: Longformer is an optimized transformer for long sequences.
- [[BigBird]]: A Sparse Attention-based model that extends Longformer with random attention patterns.
- [[Document Classification]]: One of the primary use cases for Longformer.
- [[Self-Attention]]: Longformer’s Sparse Attention is a variation of standard Self-Attention.
- [[Efficient Transformers]]: Longformer is part of this broader class of optimized transformer models.

---

## Aliases
- Longformer
- Longformer Transformer
- Sparse Longformer
- Long Sequence Transformer

---

## Tags
#longformer #transformers #sparse-attention #deep-learning #NLP #document-classification

---

## Links to Explore
- [[Sparse Attention]]: Learn how Longformer reduces complexity for long sequences.
- [[Transformers]]: Understand the architecture Longformer builds upon.
- [[BigBird]]: Compare Longformer with other Sparse Attention-based models.
- [[Efficient Transformers]]: Explore other models optimized for long sequences.
- [[Document Classification]]: A primary application of Longformer.