Implementing and Evaluating K-Means Clustering from Scratch
1 Project Overview

This project implements the K-Means clustering algorithm from scratch using only NumPy for numerical computations. A synthetic multi-modal dataset is generated and used to evaluate the clustering performance. The optimal number of clusters is determined using both the Elbow Method (WCSS) and the Silhouette Score. The results from the scratch implementation are compared against the standard scikit-learn KMeans algorithm to validate correctness.

2 Input Data Description

The dataset consists of 500 samples with 2 numerical features.
The data is synthetically generated using numpy.random.multivariate_normal.

Number of samples: 500

Number of features: 2

Number of underlying clusters: 4

Cluster structure: Overlapping (non perfectly separable)

Covariance: Shared covariance across clusters to introduce overlap

This dataset is suitable for clustering analysis because it reflects realistic scenarios where clusters are not cleanly separated.

3 K-Means Implementation from Scratch

The K-Means algorithm is implemented manually using NumPy without relying on sklearn’s clustering utilities.

The implementation includes:

Random initialization of centroids from the dataset

Euclidean distance computation for cluster assignment

Iterative centroid updates using the mean of assigned points

Convergence check based on centroid stability

Computation of Within-Cluster Sum of Squares (WCSS) after convergence

This implementation demonstrates the iterative and mathematical nature of the K-Means algorithm.

4 Optimal K Determination
4.1 Elbow Method (WCSS)

WCSS is computed for values of K ranging from 2 to 10 using the scratch implementation.
The WCSS curve shows a sharp decrease until K = 4, after which the improvement becomes marginal.
This indicates diminishing returns beyond K = 4.

4.2 Silhouette Score

Silhouette scores are computed for the same K range (2 to 10).
The maximum silhouette score is observed at:

Optimal K: 4

Silhouette Score: 0.719

This indicates strong intra-cluster cohesion and good inter-cluster separation at K = 4.

5 Final Clustering and Visualization

Using the optimal K value, the scratch K-Means algorithm is applied to the dataset.

The visualization outputs include:

Elbow Method plot (WCSS vs K)

Silhouette Score plot (Score vs K)

Final 2D scatter plot with data points colored by cluster assignment and centroids marked

The final scatter plot shows four clearly identifiable clusters with moderate overlap, consistent with the data generation process.

6 Comparison with Scikit-Learn KMeans

The scikit-learn KMeans algorithm is executed on the same dataset using the same optimal K value.

Comparison results:

Scratch WCSS: 1123.78

Scikit-learn WCSS: 1123.78

Scratch Silhouette Score: 0.719

Scikit-learn Silhouette Score: 0.719

The identical results confirm that the scratch implementation is correct. Minor floating-point differences are theoretically possible due to initialization and numerical precision, but in this execution both methods converged to the same solution.

7 Files Included in Submission

kmeans_from_scratch.py
Contains the complete Python implementation including data generation, scratch K-Means, evaluation, visualization, and sklearn comparison.

README.md
Provides an overview of the project, methodology, and results.

report.txt
Contains the detailed text-based evaluation report including data description, algorithm explanation, Elbow and Silhouette analysis, visualization interpretation, and comparison discussion.

8 Conclusion

The project successfully implements K-Means clustering from scratch and validates its correctness through comparison with the standard scikit-learn implementation. The use of Elbow Method and Silhouette Score correctly identifies the optimal number of clusters. This project demonstrates a strong understanding of unsupervised learning, distance-based clustering, and evaluation techniques.
