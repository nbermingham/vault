## Overview
**Cosine Similarity** is a metric used to measure the similarity between two vectors in a multi-dimensional space. It calculates the cosine of the angle between the vectors, providing a value between -1 and 1. This metric is widely used in [[Natural Language Processing]], [[Information Retrieval]], and [[Recommendation Systems]].

---

## Key Concepts

### Definition
Cosine Similarity measures how similar two vectors are by focusing on their orientation rather than magnitude. It is defined as:
$$
\text{Cosine Similarity} = \frac{\mathbf{A} \cdot \mathbf{B}}{\|\mathbf{A}\| \|\mathbf{B}\|}
$$
Where:
- $(\mathbf{A} \cdot \mathbf{B})$ : Dot product of vectors $\mathbf{A}$ and $\mathbf{B}$.
- $\|\mathbf{A}\|$: Magnitude of vector $\mathbf{A}$.
- $\|\mathbf{B}\|$: Magnitude of vector $\mathbf{B}$.

### Range
- **1**: Vectors are perfectly aligned (maximum similarity).
- **0**: Vectors are orthogonal (no similarity).
- **-1**: Vectors are diametrically opposed (maximum dissimilarity).

---

## Applications

### [[Natural Language Processing]]
- Comparing word, sentence, or document embeddings (e.g., similarity between word vectors in [[Word2Vec]] or [[BERT]]).
- Text similarity tasks like document clustering, duplicate detection, and plagiarism checking.

### Information Retrieval
- Ranking search results based on the similarity between query and document vectors.
- Building vector search engines.

### Recommendation Systems
- Recommending items based on vector similarity (e.g., user-item embeddings).

### Clustering and [[Classification]]
- Used in algorithms like [[K-Means Clustering]] to compare data points.

---

## Example Use Cases

1. **Word Similarity**:
   - Measure the similarity between two words using pre-trained word embeddings.
2. **Document Similarity**:
   - Compare articles or reviews for clustering or duplicate detection.
3. **Query Matching**:
   - Match user queries to the most relevant documents or database entries.

---

## Advantages
1. **Scale-Invariant**: Focuses on vector direction, not magnitude, making it robust to scaling.
2. **Simple to Compute**: Requires only dot products and magnitudes.
3. **High Interpretability**: Provides intuitive results for similarity measurement.

---

## Disadvantages
1. **Sparse Vectors**: Performance can degrade when applied to very sparse vectors.
2. **Zero Vectors**: Cannot compute similarity if one or both vectors have zero magnitude.
3. **Ignores Magnitude**: May not reflect true similarity if vector magnitudes are meaningful.

---

## Alternatives
1. **Euclidean Distance**:
   - Measures the straight-line distance between two vectors.
2. **Jaccard Similarity**:
   - Compares the similarity between sets based on their intersections and unions.
3. **Manhattan Distance**:
   - Computes the sum of absolute differences between vector components.

---

## Tools and Libraries
- **Python**:
  - SciPy: `scipy.spatial.distance.cosine`
  - NumPy: Compute manually using dot products and norms.
- **Libraries for NLP**:
  - Gensim: Includes utilities for similarity between word or document embeddings.
  - Hugging Face: Compute similarity with pre-trained [[BERT]] embeddings.

---

## Related Topics
- [[Embeddings]]: Dense vector representations for data like text, images, or graphs.
- [[Word2Vec]]: Generates word embeddings often compared using cosine similarity.
- [[Sentence Similarity]]: Tasks that involve comparing sentences in vector space.
- [[K-Means Clustering]]: Relies on similarity metrics for grouping data points.

---

## Resources
- **Books**:
  - *Speech and Language Processing* by Jurafsky and Martin.
- **Courses**:
  - Coursera: *[[Natural Language Processing]] Specialization* by DeepLearning.AI.
- **Tutorials**:
  - Gensim documentation for similarity computations.
  - TensorFlow or PyTorch guides for embedding similarity.

---

## Tags
#cosinesimilarity #machinelearning #NLP #datascience #embeddings