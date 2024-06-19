 Cryptocurrency Clustering Analysis

 Overview

This project aims to analyze and cluster various cryptocurrencies based on their market data. The analysis involves two main approaches: clustering using the original data and clustering using PCA-transformed data. By comparing these approaches, we aim to understand the impact of dimensionality reduction on clustering results and derive meaningful insights about cryptocurrency behaviors.

 Objectives

1. Data Preparation:
   - Load and preprocess the cryptocurrency market data.
   - Normalize the data using `StandardScaler`.

2. Principal Component Analysis (PCA):
   - Apply PCA to reduce the dimensionality of the data to three principal components.
   - Understand the variance explained by each principal component.

3. K-Means Clustering:
   - Perform K-Means clustering on both the original and PCA-transformed data.
   - Determine the optimal number of clusters using the Elbow method.

4. Visual Analysis:
   - Create Elbow curves to identify the optimal number of clusters for both datasets.
   - Visualize and compare the clusters using scatter plots.

5. Insights and Conclusions:
   - Analyze the impact of using fewer features (via PCA) on clustering results.
   - Discuss the benefits and trade-offs of dimensionality reduction in clustering.

 Steps and Methodology

1. Data Loading and Preprocessing:
   - Load the cryptocurrency market data from a CSV file.
   - Set the `coin_id` column as the index.
   - Normalize the data using `StandardScaler`.

2. Principal Component Analysis (PCA):
   - Create a PCA model instance with `n_components=3`.
   - Fit and transform the scaled data using the PCA model.
   - Create a DataFrame with the PCA components.
   - Retrieve the explained variance to understand the importance of each component.

3. K-Means Clustering:
   - Initialize and fit K-Means models using the original and PCA-transformed data.
   - Compute inertia values for a range of `k` values (1 to 11) to create Elbow curves.
   - Determine the optimal number of clusters based on the Elbow curves.

4. Visual Analysis:
   - Create composite plots to contrast the Elbow curves for both datasets.
   - Visualize the clusters using scatter plots for both the original and PCA-transformed data.
   - Use `hvPlot` to enhance interactivity and insights.

5. Insights and Conclusions:
   - Discuss the impact of using fewer features via PCA on clustering results.
   - Highlight the detection of outliers, cluster compactness, and the benefits of dimensionality reduction.

 Key Findings

- Outlier Detection: Clustering with the original data can highlight unique outliers which may be less prominent in PCA-transformed data.
- Cluster Compactness: PCA-transformed data often results in more compact and well-defined clusters.
- Efficiency and Interpretability: Dimensionality reduction via PCA enhances computational efficiency and makes clusters easier to visualize and interpret.
- Trade-offs: While PCA improves cluster compactness, it may also result in some information loss, impacting cluster accuracy.

 Requirements

- Python 3.7 or higher
- Libraries: pandas, scikit-learn, matplotlib, hvplot


