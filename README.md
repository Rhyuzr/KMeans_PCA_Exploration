# Iris Data Analysis: K-means and PCA

This repository contains the code and exploratory analysis of the Iris dataset using unsupervised learning techniques: K-means clustering and Principal Component Analysis (PCA).

## Introduction
This project aims to explore the inherent structure of the Iris dataset without known labels, and to evaluate the effectiveness of combining PCA with K-means to improve clustering results.

## Methodology
The report is divided into two main parts:

### Part 1: K-means Clustering
This section focuses on applying the K-means algorithm to identify the optimal number of clusters (K) in the Iris dataset. Two common methods were used:

- **Elbow Method**: Analysis of Within-Cluster Sum of Squares (WCSS) to identify the optimal "elbow" point.
- **Silhouette Analysis**: Evaluation of clustering quality based on object similarity to their own cluster compared to neighboring clusters.

**Key Results of Part 1:**
The analyses suggested that K=2 or K=3 are potential values, with a preference for K=2 according to internal metrics (WCSS and silhouette score), reflecting an overlap between Iris-versicolor and Iris-virginica species in feature space.

### Part 2: Principal Component Analysis (PCA) and K-means
This part explores the impact of dimensionality reduction via PCA on K-means clustering performance. A custom PCA implementation was used to transform the data into a two-dimensional latent space.

- **PCA Implementation**: Data was centered, covariance matrix calculated, and eigenvectors/values were used for transformation into 2 principal components.
- **Clustering on Transformed Data**: K-means (with K=3) was applied to PCA-transformed data.

**Key Results of Part 2:**
Applying K-means to PCA-reduced data showed clearer separation between clusters in latent space. However, some overlap remained between certain class pairs, highlighting that even after dimensionality reduction, perfect distinction of all species isn't trivial due to their intrinsic feature distribution. PCA simplified the data representation, allowing K-means to better capture the global structure.

## Conclusion
This project highlights the strengths and limitations of K-means clustering and PCA for discovering unsupervised data structures. It demonstrates how dimensionality reduction can prepare data for better clustering, while emphasizing the importance of understanding inherent dataset characteristics that may influence clustering results.
