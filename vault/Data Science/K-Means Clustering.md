## Overview
**K-Means Clustering** is a popular unsupervised [[Clustering]] algorithm that partitions a dataset into \( K \) clusters. It minimizes the variance within each cluster by assigning data points to the nearest cluster center. K-Means is widely used for tasks such as customer segmentation, image compression, and pattern recognition.

---

## Key Concepts

### Objective Function
K-Means minimizes the **intra-cluster variance** by optimizing the following objective:
$$
J = \sum_{i=1}^K \sum_{x \in C_i} \|x - \mu_i\|^2
$$
Where:
- $K$: Number of clusters.
- $C_i$: Set of points in cluster $i$.
- $\mu_i$: Centroid (mean) of cluster $i$.

### Centroid
- Each cluster is represented by a **centroid**, which is the mean position of all points in that cluster.
- Centroids are updated iteratively during the algorithm.

---

## How K-Means Works

1. **Initialization**:
   - Randomly select \( K \) data points as the initial centroids.

2. **Assignment Step**:
   - Assign each data point to the cluster with the nearest centroid (based on a distance metric, typically Euclidean distance).

3. **Update Step**:
   - Recalculate the centroids as the mean of all points assigned to each cluster.

4. **Repeat**:
   - Alternate between the assignment and update steps until centroids no longer change significantly or a maximum number of iterations is reached.

---

## Parameters

1. **Number of Clusters $K$**:
   - The number of clusters must be predefined.
   - Methods like the **[[Elbow Method]]** or **[[Silhouette Score]]** help determine the optimal $K$.

2. **Distance Metric**:
   - Typically uses [[Euclidean distance]] but can be modified for specific use cases.

3. **Max Iterations**:
   - Limits the number of iterations for the algorithm.

4. **Initialization Method**:
   - **Random Initialization**: Randomly selects initial centroids.
   - **[[K-Means++]]**: Ensures better initial centroid selection to improve convergence.

---

## Advantages

1. **Simplicity**:
   - Easy to understand and implement.
2. **Scalability**:
   - Works well on large datasets, especially with optimizations like mini-batch K-Means.
3. **Speed**:
   - Computationally efficient compared to other clustering algorithms.

---

## Disadvantages

1. **Predefined \( K \)**:
   - Requires the number of clusters to be set beforehand.
2. **Sensitivity to Initialization**:
   - Poor initialization can lead to suboptimal results.
3. **Assumes Spherical Clusters**:
   - Struggles with non-spherical or overlapping clusters.
4. **Outlier Sensitivity**:
   - Outliers can significantly affect cluster centroids.

---

## Applications

1. **Customer Segmentation**:
   - Groups customers based on purchasing behavior or demographic data.
2. **Image Compression**:
   - Reduces the number of colors in an image by clustering pixels.
3. **Anomaly Detection**:
   - Identifies outliers by assigning them to small or no clusters.
4. **Document Clustering**:
   - Clusters text documents based on [[TF-IDF]] or word embeddings.

---

## Example Workflow

1. **Preprocess Data**:
   - Scale features (e.g., using standardization or normalization) for better performance.
2. **Apply K-Means**:
   - Run the K-Means algorithm with different \( K \) values.
3. **Evaluate Clusters**:
   - Use metrics like the **Silhouette Score** or the **Elbow Method** to assess the quality of clustering.
4. **Interpret Results**:
   - Analyze the centroids and the distribution of points within clusters.

---

## Evaluation Metrics

1. **Elbow Method**:
   - Plots the within-cluster sum of squares (WCSS) against \( K \) and identifies the "elbow" where adding more clusters has diminishing returns.
2. **Silhouette Score**:
   - Measures how similar points are to their own cluster versus other clusters (range: -1 to 1).
3. **Inertia**:
   - Measures the compactness of clusters by summing squared distances from each point to its assigned centroid.

---

## Comparison with Other Clustering Methods

| Feature                | K-Means   | [[DBSCAN]] | [[HDBSCAN]] |
| ---------------------- | --------- | ---------- | ----------- |
| **Predefined \( K \)** | Yes       | No         | No          |
| **Handles Noise**      | No        | Yes        | Yes         |
| **Cluster Shape**      | Spherical | Arbitrary  | Arbitrary   |
| **Scalability**        | High      | Moderate   | Low         |

---

## Related Topics

- [[DBSCAN]]: An alternative clustering method that does not require \( K \).
- [[HDBSCAN]]: Extends DBSCAN for varying densities.
- [[Dimensionality Reduction]]: Techniques like [[Principal Component Analysis]] or [[UMAP]] are often used to preprocess data for K-Means.
- [[Anomaly Detection]]: K-Means can indirectly identify anomalies as points far from centroids.

---

## Tools and Libraries

1. **[[Scikit-learn]]**:
   - Provides efficient implementations of K-Means and Mini-Batch K-Means.
2. **TensorFlow/PyTorch**:
   - Allows custom implementations of K-Means for neural networks.
3. **Matplotlib/Seaborn**:
   - Visualize clusters using scatter plots.

---

## Resources

### Tutorials
- [[Scikit-learn]] documentation on K-Means.
- Online tutorials on clustering and unsupervised learning.

### Books
- *Hands-On Machine Learning with [[Scikit-learn]], Keras, and TensorFlow* by Aurélien Géron.
- *Introduction to Statistical Learning* by James et al.

---

## Tags
#KMeans #clustering #unsupervised-learning #machinelearning #datavisualization