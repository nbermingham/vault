## Overview
A **Co-occurrence Matrix** is a matrix that captures the frequency with which pairs of items (e.g., words, entities) appear together in a given context. It is widely used in [[Natural Language Processing]] (NLP) and other fields to model relationships between items.

---

## Key Concepts

### Definition
- A co-occurrence matrix is a square matrix where:
  - Rows and columns represent items (e.g., words in a vocabulary).
  - Each cell $(i, j)$ represents the co-occurrence count of item $i$ and item $j$  in a specific context (e.g., within a window of words).

### Context Window
- Defines the range within which items are considered co-occurring.
- Example:
  - Sentence: "The cat sat on the mat."
  - With a window size of 2, "cat" co-occurs with "The," "sat," and "on."

### Sparsity
- Co-occurrence matrices are often sparse, as most word pairs do not co-occur frequently in natural text.

---

## Mathematical Representation

Let \( V \) be the size of the vocabulary:
- A co-occurrence matrix \( C \) is a \( V \times V \) matrix, where:
$$
C_{ij} = \text{Number of times word } w_i \text{ co-occurs with word } w_j.
$$

---

## Applications

### [[Word Embeddings]]
- **[[GloVe ]](Global Vectors)**:
  - Learns word embeddings by factorizing the co-occurrence matrix.
- **[[Latent Semantic Analysis]] (LSA)**:
  - Decomposes the co-occurrence matrix to capture semantic relationships.

### [[Text Similarity]]
- Measures similarity between words or documents based on their co-occurrence patterns.

### [[Graph Representation]]
- Can represent relationships in a network, where nodes are items and edges are co-occurrence frequencies.

### [[Collaborative Filtering]]
- Used in recommendation systems to capture item-user relationships.

---

## Example

### Sentence
"The quick brown fox jumps over the lazy dog."

### Vocabulary
$V = [\text{"the"}, \text{"quick"}, \text{"brown"}, \text{"fox"}, \text{"jumps"}, \text{"over"}, \text{"lazy"}, \text{"dog"}]$

### Co-occurrence Matrix with Window Size = 2
$$
\begin{bmatrix}
 & \text{the} & \text{quick} & \text{brown} & \text{fox} & \text{jumps} & \text{over} & \text{lazy} & \text{dog} \\
\text{the} & 0 & 2 & 1 & 0 & 0 & 0 & 1 & 0 \\
\text{quick} & 2 & 0 & 1 & 1 & 0 & 0 & 0 & 0 \\
\text{brown} & 1 & 1 & 0 & 1 & 0 & 0 & 0 & 0 \\
\text{fox} & 0 & 1 & 1 & 0 & 1 & 0 & 0 & 0 \\
\text{jumps} & 0 & 0 & 0 & 1 & 0 & 1 & 0 & 0 \\
\text{over} & 0 & 0 & 0 & 0 & 1 & 0 & 1 & 0 \\
\text{lazy} & 1 & 0 & 0 & 0 & 0 & 1 & 0 & 1 \\
\text{dog} & 0 & 0 & 0 & 0 & 0 & 0 & 1 & 0
\end{bmatrix}
$$

---

## [[Normalization]]
- **[[Row Normalization]]**:
  - Converts counts to probabilities by dividing each row by its sum.
$$
P(w_j | w_i) = \frac{C_{ij}}{\sum_k C_{ik}}
$$
- **[[PPMI (Positive Pointwise Mutual Information)]]**:
  - Measures the strength of association between two words:
$$
PPMI(w_i, w_j) = \max\left(0, \log \frac{P(w_i, w_j)}{P(w_i)P(w_j)}\right)
$$
Where:
  - $P(w_i, w_j) = \frac{C_{ij}}{\sum_{i,j} C_{ij}}$
  - $P(w_i) = \frac{\sum_j C_{ij}}{\sum_{i,j} C_{ij}}$

---

## Advantages
1. **Simplicity**:
   - Easy to construct and interpret.
2. **Captures Semantic Relationships**:
   - Words with similar meanings often have similar co-occurrence patterns.
3. **Foundation for Advanced Models**:
   - Used in word embedding methods like [[GloVe]] and [[Latent Semantic Analysis (LSA)]].

---

## Disadvantages
1. **High Dimensionality**:
   - For large vocabularies, the matrix becomes very large and sparse.
2. **Context Limitations**:
   - Relies on predefined context windows, which may not capture all relationships.
3. **Data Sparsity**:
   - Many word pairs will have zero or low co-occurrence counts, especially in small corpora.

---

## Tools and Libraries

### Python Libraries
- **[[NumPy]]**:
  - Used to construct and manipulate co-occurrence matrices.
- **[[SciPy]]**:
  - Efficient sparse matrix storage and operations.
- **[[Gensim]]**:
  - Includes utilities for constructing co-occurrence matrices.
- **[[NLTK]] and [[SpaCy]]**:
  - Tokenization and pre-processing pipelines to build matrices.

---

## Related Topics
- [[GloVe]]: Word embeddings based on co-occurrence matrices.
- [[Latent Semantic Analysis]]: Dimensionality reduction of co-occurrence matrices.
- [[Word Embeddings]]: Dense representations of words derived from co-occurrence.
- [[PPMI]]: Normalization technique to enhance matrix interpretability.

---

## Resources

### Books
- *Speech and Language Processing* by Jurafsky and Martin.
- *Deep Learning for [[Natural Language Processing]]* by Palash Goyal et al.

### Courses
- Coursera: *Natural Language Processing Specialization* by DeepLearning.AI.
- Udemy: *NLP Fundamentals with Python*.

### Tutorials
- Gensim documentation for co-occurrence matrix construction.
- Blog posts on PPMI and GloVe implementations.

---

## Tags
#cooccurrencematrix #NLP #wordembeddings #datascience #representationlearning