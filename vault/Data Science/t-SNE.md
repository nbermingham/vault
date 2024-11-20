## Overview
**t-SNE (t-Distributed Stochastic Neighbor Embedding)** is a non-linear [[Dimensionality Reduction]] technique designed for visualizing high-dimensional data in two or three dimensions. It preserves the local structure of the data, making it especially effective for tasks like clustering and exploratory [[Data Analysis]]. Unlike linear techniques such as [[PCA]], t-SNE focuses on maintaining neighborhood relationships rather than preserving global structure.

---

## Key Concepts

1. **Probabilistic Similarity**:
   - t-SNE converts high-dimensional pairwise distances into probabilities representing similarity between points.
   - Points close to each other have high similarity, while distant points have low similarity.

2. **[[Kullback-Leibler Divergence]]**:
   - The algorithm minimizes the divergence between similarity distributions in high-dimensional and low-dimensional spaces.

3. **[[Non-linear Transformation]]**:
   - t-SNE emphasizes local relationships, often revealing clusters that linear methods like [[PCA]] may not detect.

---

## Steps in t-SNE

1. **Compute Pairwise Similarities**:
   - In high-dimensional space, pairwise similarities are computed using a Gaussian kernel.

2. **Construct Low-Dimensional Mapping**:
   - Pairwise similarities in the low-dimensional space are modeled using a Student-t distribution to handle dense clusters.

3. **Optimize Embedding**:
   - Minimize the Kullback-Leibler divergence between high-dimensional and low-dimensional similarity distributions.

---

## Advantages

1. **Effective Visualization**:
   - Excellent for visualizing patterns and clusters in high-dimensional data.
   
2. **Captures Local Structure**:
   - Focuses on preserving relationships between neighboring data points.
   
3. **Non-linear**:
   - Suitable for uncovering non-linear patterns that linear methods like [[PCA]] may miss.

---

## Disadvantages

1. **Computationally Expensive**:
   - t-SNE has high time and memory complexity, especially for large datasets.
   
2. **Loss of Global Structure**:
   - Prioritizes local neighborhood relationships over global data relationships.
   
3. **Hyperparameter Sensitivity**:
   - Results are highly dependent on parameters like perplexity and learning rate, requiring careful tuning.

---

## Applications

1. **Clustering**:
   - Commonly used to visualize clustering results in tasks like [[Natural Language Processing]] and [[Image Recognition]].
   
2. **Exploratory Data Analysis**:
   - Helps understand high-dimensional data by reducing it to interpretable 2D or 3D visualizations.
   
3. **Genomics and Biology**:
   - Widely applied in fields like single-cell RNA-seq data analysis.

---

## Related Topics

- [[Dimensionality Reduction]]: t-SNE is a non-linear method for reducing dimensions.
- [[PCA]]: A linear dimensionality reduction technique often compared with t-SNE.
- [[UMAP]]: Another non-linear dimensionality reduction method, faster and sometimes preferred over t-SNE.
- [[Clustering]]: t-SNE is frequently used to visualize clustering results.
- [[Data Visualization]]: t-SNE enables effective visualization of high-dimensional data.

---

## Tools and Libraries

1. **Python Libraries**:
   - `scikit-learn`: Provides an implementation of t-SNE.
   - `openTSNE`: Optimized and scalable t-SNE implementation.
   - `PyTorch`/`TensorFlow`: t-SNE can be implemented manually or through extensions.

2. **Visualization Tools**:
   - `matplotlib` or `seaborn`: For 2D and 3D visualizations.
   - `Plotly`: For interactive visualizations.

---

## Aliases
- t-SNE
- t-Distributed Stochastic Neighbor Embedding
- t-SNE Algorithm
- Non-linear Dimensionality Reduction (t-SNE)
- Data Visualization with t-SNE
- High-Dimensional Visualization (t-SNE)

---

## Tags
#t-SNE #dimensionality-reduction #data-visualization #non-linear-algorithms #machinelearning