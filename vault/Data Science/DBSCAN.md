## Overview
**DBSCAN (Density-Based Spatial Clustering of Applications with Noise)** is a density-based clustering algorithm that groups data points based on their density in the feature space. It is widely used for identifying clusters of arbitrary shape and isolating noise (outliers) in the dataset. Unlike [[K-Means Clustering]], DBSCAN does not require the number of clusters to be predefined.

DBSCAN was introduced by Ester et al. in 1996 and remains a popular choice for [[Clustering]] tasks in [[Machine Learning]].

---

## Key Concepts

### [[Density-Based Clustering]]
- DBSCAN groups points that are closely packed together, while points in low-density regions are treated as noise.
- A cluster is defined as a region where the density of points exceeds a certain threshold.

### Definitions
1. **Core Point**:
   - A point with at least `min_samples` neighbors within a radius `eps`.
2. **Border Point**:
   - A point that is not a core point but lies within the `eps` radius of a core point.
3. **Noise Point**:
   - A point that is neither a core point nor a border point.

---

## How DBSCAN Works

1. **Select a Random Point**:
   - If it has at least `min_samples` neighbors within `eps`, it becomes a core point and forms a cluster.
   - If not, it is marked as noise (temporarily, as it may later belong to a cluster).

2. **Expand the Cluster**:
   - Recursively add all density-reachable points (within `eps`) to the cluster.

3. **Repeat**:
   - Continue the process until all points are visited.

4. **Handle Noise**:
   - Points that cannot be assigned to any cluster are labeled as noise.

---

## Parameters

1. **eps (Epsilon)**:
   - Defines the radius of the neighborhood around a point.
   - A smaller `eps` detects finer clusters but may leave more points as noise.

2. **min_samples**:
   - Minimum number of points required to form a dense region (core point).
   - Higher values result in larger, denser clusters but may miss smaller ones.

3. **metric**:
   - The distance metric used to calculate the distance between points (e.g., Euclidean, Manhattan, cosine).

---

## Advantages

1. **Arbitrary Cluster Shapes**:
   - Detects clusters of varying shapes and sizes, unlike [[K-Means Clustering]].
2. **Handles Noise**:
   - Explicitly identifies and labels noise points.
3. **No Predefined Clusters**:
   - Automatically determines the number of clusters based on the data.

---

## Disadvantages

1. **Parameter Sensitivity**:
   - The results depend heavily on the choice of `eps` and `min_samples`.
2. **Poor Performance on Sparse Data**:
   - Struggles with datasets with varying densities or high-dimensional data.
3. **Scalability**:
   - Computationally intensive for large datasets, especially when `eps` is small.

---

## Applications

1. **Anomaly Detection**:
   - Identifies outliers as noise in datasets.
2. **Geospatial Analysis**:
   - Groups spatial points, such as customer locations or geographical data.
3. **Market Segmentation**:
   - Clusters customer data based on purchase behavior or preferences.
4. **Biological Data**:
   - Identifies clusters in gene expression or other biological datasets.

---

## Example Workflow

1. **Preprocess Data**:
   - Normalize features and handle missing values.
2. **Run DBSCAN**:
   - Apply DBSCAN with suitable `eps` and `min_samples` values.
3. **Evaluate Results**:
   - Use visualizations (e.g., scatterplots) to inspect clusters and noise points.
4. **Adjust Parameters**:
   - Tune `eps` and `min_samples` for better cluster identification.

---

## Tools and Libraries

1. **Python Libraries**:
   - **[[Scikit-learn]]**: Implements DBSCAN (`sklearn.cluster.DBSCAN`).
   - **[[HDBSCAN]]**: An extension of DBSCAN for varying density clusters.
2. **Visualization**:
   - Use [[UMAP]] or t-SNE for visualizing high-dimensional data.

---

## Comparison with Other Clustering Methods

| Feature               | DBSCAN                           | K-Means                          | [[HDBSCAN]]                          |
|-----------------------|-----------------------------------|-----------------------------------|-----------------------------------|
| **Cluster Shape**     | Arbitrary                        | Spherical                        | Arbitrary                        |
| **Handles Noise**     | Yes                              | No                               | Yes                              |
| **Predefined Clusters** | No                              | Yes                              | No                               |
| **Varying Densities** | No                               | No                               | Yes                              |

---

## Related Topics

- [[HDBSCAN]]: An extension of DBSCAN for hierarchical and varying density clustering.
- [[K-Means Clustering]]: A clustering algorithm that assumes spherical clusters.
- [[Dimensionality Reduction]]: Techniques like [[UMAP]] or [[Principal Component Analysis]] are often applied before clustering.
- [[Anomaly Detection]]: DBSCAN is widely used to identify outliers.

---

## Resources

### Research Papers
- *A Density-Based Algorithm for Discovering Clusters in Large Spatial Databases with Noise* (Ester et al., 1996).

### Tutorials
- [[Scikit-learn]] documentation on DBSCAN.
- Online guides for parameter tuning and evaluation.

### Books
- *Hands-On Machine Learning with [[Scikit-learn]], Keras, and TensorFlow* by Aurélien Géron.

---

## Tags
#DBSCAN #clustering #unsupervised-learning #machinelearning #density-based-clustering