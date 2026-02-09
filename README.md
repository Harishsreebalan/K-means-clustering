K Means Clustering From Scratch Using NumPy

Project Description
This project implements and evaluates the K Means clustering algorithm from scratch using NumPy. The complete algorithm was executed on a synthetic dataset and validated by comparing the results with the standard scikit learn KMeans implementation.

Input Data Characteristics
1 Total number of samples 500
2 Number of features 2
3 Data type Synthetic numerical data
4 Data generation method numpy random multivariate normal
5 Number of clusters used during data generation 4
6 Clusters are overlapping and not perfectly separable

Completed Technical Tasks
1 Generated a synthetic dataset of 500 samples
2 Implemented K Means clustering from scratch using NumPy
3 Determined the optimal number of clusters using Elbow Method and Silhouette Score
4 Visualized clustering results using two dimensional scatter plots
5 Compared scratch implementation results with scikit learn KMeans

Algorithm Execution
The K Means algorithm was initialized with random centroids. Euclidean distance was used to assign data points to the nearest centroid. Centroids were updated iteratively until convergence. Within Cluster Sum of Squares was calculated after convergence.

K Optimization Analysis
K values evaluated ranged from 2 to 10
Elbow Method showed a clear reduction in WCSS improvement beyond K equal to 4
Silhouette Score reached its maximum at K equal to 4
The final selected optimal K value was 4

Final Quantitative Results
Scratch K Means WCSS 1123.78
Scikit learn KMeans WCSS 1123.78
Scratch Silhouette Score 0.719
Scikit learn Silhouette Score 0.719

Result Interpretation
The optimal K value of 4 correctly identifies the underlying cluster structure of the dataset. The scratch implementation produces identical WCSS and silhouette scores when compared with scikit learn KMeans. This confirms the correctness and accuracy of the scratch implementation.

Visualization Summary
Elbow curve demonstrates diminishing improvement in WCSS beyond K equal to 4
Silhouette plot confirms maximum cluster separation at K equal to 4
Final scatter plot shows four distinct overlapping clusters with clearly defined centroids

Execution Confirmation
All results plots and metrics were produced by executing the full Python implementation in a single Jupyter Notebook cell.
