## Overview
**HDBSCAN (Hierarchical Density-Based Spatial Clustering of Applications with Noise)** is an advanced clustering algorithm based on the [[DBSCAN]] algorithm. It is designed to identify clusters of varying densities and handle noise more effectively. HDBSCAN is widely used for [[Clustering]] in applications such as anomaly detection, text analysis, and biological data analysis.

Unlike [[DBSCAN]], HDBSCAN builds a hierarchical clustering model and extracts clusters from it based on stability, making it more flexible and robust for datasets with varying cluster densities.

---

## Key Concepts

### Differences from [[DBSCAN]]
- **Varying Densities**:
  - [[DBSCAN]] assumes clusters have uniform density, while HDBSCAN can identify clusters with varying densities.
- **Hierarchy**:
  - HDBSCAN creates a hierarchy of clusters and chooses the most stable ones, enabling better cluster selection.
- **Parameter Tuning**:
  - HDBSCAN reduces the sensitivity to the choice of parameters compared to [[DBSCAN]].

### Key Terminology
1. **Minimum Cluster Size**:
   - The smallest size of a cluster that HDBSCAN will consider.
2. **Core Distance**:
   - The distance from a point to its \( k \)-th nearest neighbor.
3. **Mutual Reachability Distance**:
   - Combines core distance and the distance between points to handle clusters with varying densities.

---

## How HDBSCAN Works

1. **Compute Mutual Reachability Distance**:
   - Create a distance graph based on the mutual reachability distance of data points.

2. **Construct a Minimum Spanning Tree**:
   - Build a graph that represents the connectivity of points based on their mutual reachability distances.

3. **Hierarchical Clustering**:
   - Create a hierarchy by iteratively removing edges from the graph to split clusters.

4. **Extract Clusters**:
   - Select stable clusters from the hierarchy based on their persistence.

5. **Label Noise**:
   - Points that do not belong to any stable cluster are labeled as noise.

---

## Advantages

1. **Handles Varying Densities**:
   - Adapts to clusters of different densities, making it more versatile than [[DBSCAN]].
2. **Identifies Noise**:
   - Effectively separates noise points from clusters.
3. **No Predefined Number of Clusters**:
   - Automatically determines the number of clusters based on data.
4. **Hierarchical Representation**:
   - Provides a dendrogram-like view for interpreting cluster relationships.

---

## Disadvantages

1. **Computational Complexity**:
   - More computationally intensive than DBSCAN, especially for large datasets.
2. **Parameter Sensitivity**:
   - Requires careful tuning of `min_cluster_size` and `min_samples` for optimal results.
3. **Not Deterministic**:
   - Results can vary depending on the random seed used.

---

## Parameters

1. **min_cluster_size**:
   - The minimum size of clusters to be considered.
   - Smaller values detect more fine-grained clusters but may overfit noise.

2. **min_samples**:
   - Determines the number of neighbors required to classify a point as dense.
   - Higher values make the algorithm more conservative.

3. **metric**:
   - The distance metric used to compute distances (e.g., Euclidean, Manhattan, cosine).

---

## Applications

1. **Anomaly Detection**:
   - Identifies outliers as noise in datasets.
2. **Text Analysis**:
   - Clusters documents or word embeddings based on semantic similarity.
3. **Biological Data**:
   - Groups gene expression data or other high-dimensional biological datasets.
4. **Market Segmentation**:
   - Clusters customer data for targeted marketing.

---

## Example Workflow

1. **Preprocess Data**:
   - Normalize and scale the data to ensure uniform metrics.
2. **Run HDBSCAN**:
   - Use the HDBSCAN algorithm to identify clusters and noise.
3. **Visualize Results**:
   - Use dimensionality reduction techniques like [[UMAP]] to visualize clusters.
4. **Interpret Clusters**:
   - Analyze cluster labels and noise points for insights.

---

## Tools and Libraries

1. **Python Libraries**:
   - **HDBSCAN**: The official Python implementation (`hdbscan` library).
   - **[[Scikit-learn]]**: Can integrate HDBSCAN outputs for further analysis.
2. **Visualization**:
   - Combine with [[UMAP]] for low-dimensional visualization of clusters.

---

## Comparison with Other Clustering Methods

| Feature               | HDBSCAN                           | [[DBSCAN]]                            | K-Means                           |
|-----------------------|------------------------------------|------------------------------------|------------------------------------|
| **Varying Densities** | Yes                               | No                                | No                                |
| **Handles Noise**     | Yes                               | Yes                               | No                                |
| **Predefined Clusters** | No                               | No                                | Yes                               |
| **Hierarchical**      | Yes                               | No                                | No                                |

---

## Related Topics

- [[DBSCAN]]: The foundational algorithm for HDBSCAN.
- [[UMAP]]: Often used for visualizing clusters created by HDBSCAN.
- [[Clustering]]: HDBSCAN is a powerful tool in unsupervised clustering tasks.

---

## Resources

### Research Papers
- *HDBSCAN: Hierarchical Density-Based Spatial Clustering of Applications with Noise* by Campello et al. (2013).

### Tutorials
- Official HDBSCAN Python library documentation.
- Python tutorials for HDBSCAN with practical examples.

### Books
- *Hands-On Machine Learning with [[Scikit-learn]], Keras, and TensorFlow* by Aurélien Géron.

---

## Tags
#HDBSCAN #clustering #unsupervised-learning #machinelearning #density-based-clustering