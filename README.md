K Means Clustering From Scratch Using NumPy

Project Overview
This project implements the K Means clustering algorithm from scratch using NumPy. The main goal is to understand the internal working of K Means without relying on built in machine learning libraries. The project also compares the scratch implementation with the standard scikit learn implementation for verification.

Objectives
1 Implement K Means clustering from scratch using NumPy
2 Generate a synthetic dataset for clustering
3 Identify the optimal number of clusters
4 Visualize clustering results
5 Compare scratch implementation with scikit learn

Dataset Description
1 Type Synthetic dataset
2 Total samples 500
3 Number of features 2
4 Number of clusters 4
5 Data generation method numpy random multivariate normal
6 Clusters are overlapping and not perfectly separable

Technologies Used
1 Python
2 NumPy
3 Matplotlib
4 Scikit learn for comparison only

Algorithm Description
1 Randomly initialize centroids
2 Compute Euclidean distance between data points and centroids
3 Assign each point to the nearest centroid
4 Update centroids based on cluster mean
5 Repeat until convergence
6 Compute within cluster sum of squares

Optimal Cluster Selection
1 K values tested from 2 to 10
2 Elbow method used to analyze WCSS
3 Silhouette score used to measure cluster quality
4 Optimal K selected based on highest silhouette score

Visualization
1 Elbow curve for WCSS
2 Silhouette score plot
3 Two dimensional scatter plot showing clusters and centroids

Comparison With Scikit Learn
1 Scratch K Means WCSS compared with scikit learn inertia
2 Scratch silhouette score compared with scikit learn silhouette score
3 Results are similar with minor variation due to random initialization

How To Run
1 Open Jupyter Notebook or Google Colab
2 Paste the complete code into a single cell
3 Run the cell to view output and plots

Project Structure
1 Single Python notebook file
2 README text file
