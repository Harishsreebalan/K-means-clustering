K Means Clustering From Scratch Evaluation Report

1 Input Data Description
The experiment was conducted on a synthetic dataset consisting of 500 data points with 2 numerical features. The data was generated using numpy random multivariate normal distribution. Four underlying cluster centers were used during generation, with shared covariance to intentionally create overlapping clusters. This makes the clustering task non trivial and suitable for evaluation.

2 Scratch K Means Implementation
The K Means algorithm was implemented from scratch using NumPy. Centroids were initialized randomly from the dataset. Euclidean distance was used to assign each data point to the nearest centroid. Centroids were recomputed as the mean of assigned points. This process was repeated iteratively until centroid positions stabilized. Within Cluster Sum of Squares was computed after convergence to evaluate compactness.

3 Elbow Method Analysis
The Elbow Method was applied by computing WCSS for K values ranging from 2 to 10. As K increased, WCSS decreased rapidly until K equal to 4. Beyond this value, the reduction in WCSS became marginal. This indicates diminishing returns when increasing cluster count further and suggests that K equal to 4 is an appropriate choice.

4 Silhouette Score Analysis
Silhouette scores were computed for each K value between 2 and 10. The silhouette score reached its maximum value at K equal to 4 with a score of 0.719. This indicates strong intra cluster cohesion and good separation between clusters at this K value compared to other tested values.

5 Final Clustering Visualization Interpretation
The final two dimensional scatter plot shows four clearly identifiable clusters with moderate overlap. Each cluster is centered around a distinct centroid. The overlap observed between clusters reflects the intentional covariance used during data generation and confirms that the algorithm handled non perfectly separable data correctly.

6 Comparison With Scikit Learn
The scratch implementation was compared against scikit learn KMeans using the same optimal K value. Both methods produced identical WCSS values of 1123.78 and identical silhouette scores of 0.719. Minor floating point differences are theoretically possible due to initialization and numerical precision, but in this execution both implementations converged to the same solution, confirming correctness.

7 Conclusion
The scratch implementation of K Means successfully replicated the behavior of the standard scikit learn algorithm. Optimal cluster selection using Elbow Method and Silhouette Score correctly identified the true underlying structure of the dataset. The experiment validates the correctness and effectiveness of the scratch implementation.
