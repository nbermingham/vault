## Overview
The **Dot Product** is a fundamental operation in [[Linear Algebra]] that measures the similarity between two [[Vectors]]. It is widely used in [[Machine Learning]], [[Deep Learning]], and [[Data Science]] for tasks such as [[Feature Similarity]], [[Cosine Similarity]], and projections.

The Dot Product combines two vectors into a scalar value by multiplying their corresponding components and summing the results. It plays a critical role in operations like [[Matrix Multiplication]] and in algorithms such as [[Gradient Descent]].

---

## Formula
For two vectors $a = [a_1, a_2, \dots, a_n]$ and $b = [b_1, b_2, \dots, b_n]$, the Dot Product is:
$$
a \cdot b = \sum_{i=1}^n a_i b_i = a_1 b_1 + a_2 b_2 + \dots + a_n b_n
$$

Alternatively, it can be expressed using magnitudes and the cosine of the angle $\theta$ between the vectors:
$$
a \cdot b = \|a\| \|b\| \cos \theta
$$
Where:
- $\|a\|$: [[Norm]] (magnitude) of vector $a$.
- $\|b\|$: [[Norm]] (magnitude) of vector $b$.
- $\cos \theta$: Cosine of the angle between $a$ and $b$.

---

## Key Concepts

### 1. **Geometric Interpretation**
- The Dot Product measures the extent to which two vectors point in the same direction:
  - $a \cdot b > 0$: Vectors point in roughly the same direction.
  - $a \cdot b = 0$: Vectors are orthogonal (perpendicular).
  - $a \cdot b < 0$: Vectors point in opposite directions.

### 2. **Projection**
- The Dot Product can be used to project one vector onto another:
  $$
  \text{Projection of } a \text{ onto } b = \frac{a \cdot b}{\|b\|}
  $$

### 3. **Similarity Measure**
- The Dot Product is foundational to [[Cosine Similarity]], which normalizes the Dot Product to measure the angular similarity between vectors.

---

## Applications

1. **[[Machine Learning]]**:
   - Measures similarity between [[Feature Vectors]].
   - Used in distance metrics like [[Cosine Similarity]].

2. **[[Deep Learning]]**:
   - Computes activations in [[Neural Networks]] during [[Forward Propagation]].
   - Integral to [[Backpropagation]] for gradient calculations.

3. **[[Matrix Multiplication]]**:
   - Each element of the resulting matrix in a [[Matrix Multiplication]] is computed as the Dot Product of a row vector and a column vector.

4. **[[Dimensionality Reduction]]**:
   - Projects data points onto lower-dimensional subspaces in methods like [[PCA]].

5. **[[Computer Vision]]**:
   - Finds similarity between image feature vectors.

6. **[[Natural Language Processing]]**:
   - Calculates similarity between [[Word Embeddings]] such as [[Word2Vec]] or [[GloVe]].

---

## Advantages

1. **Simplicity**:
   - Easy to compute and interpret.

2. **Efficiency**:
   - Computationally inexpensive, even for high-dimensional data.

3. **Versatility**:
   - Applicable in a wide range of fields, including [[Physics]], [[Data Science]], and [[Computer Vision]].

---

## Disadvantages

1. **Lack of Scale Independence**:
   - The Dot Product is affected by the magnitudes of the vectors, which can be mitigated by normalization (e.g., [[Cosine Similarity]]).

2. **Non-Symmetry**:
   - The Dot Product is not symmetric under rotation in non-Euclidean spaces.

---

## Related Topics

- [[Vectors]]: The fundamental objects operated on by the Dot Product.
- [[Matrix Multiplication]]: The Dot Product forms the basis of [[Matrix Multiplication]].
- [[Cosine Similarity]]: Normalizes the Dot Product for angular similarity.
- [[Norms]]: Measure the magnitude of vectors, used in Dot Product normalization.
- [[PCA]]: Uses Dot Products to project data onto principal components.
- [[Backpropagation]]: Relies on Dot Products for gradient computations.
- [[Word Embeddings]]: The Dot Product measures similarity between embeddings in [[NLP]].

---

## Aliases
- Dot Product
- Scalar Product
- Inner Product
- Vector Multiplication
- Projection Product

---

## Tags
#dot-product #linear-algebra #vectors #matrix-multiplication #machinelearning #deeplearning #similarity