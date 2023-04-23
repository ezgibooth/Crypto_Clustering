# Crypto Clustering

The goal of this challenge is to use Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

First, we looked at the scaled price change values of all cryptocurrencies for different time periods.
<p align="center">
<img src="https://user-images.githubusercontent.com/118090932/233820843-50fdf9c0-833c-46ce-bf15-b1c37e0f7e81.png" width="650" height="400">
</p>


## Deliverable 1: Find the Best Value for k Using the Original Scaled DataFrame

Using the scaled data, we created an elbow curve to determine the optimal k-value for data clustering. Based on this, the best value for k is 4.

<p align="center">
<img src="https://user-images.githubusercontent.com/118090932/233820979-30f46486-f2c1-44d4-8ed5-d421e69a729d.png" width="600" height="300">
</p>

## Deliverable 2: Cluster Cryptocurrencies with K-means Using the Original Scaled Data

Below is a plot of all the cryptocurrencies based on the predicted clusters from K-means modeling using the original scaled data.

<p align="center">
<img src="https://user-images.githubusercontent.com/118090932/233821050-65e2be38-b7e7-442f-8de5-dd82fa13ba00.png" width="600" height="300">
</p>

## Deliverable 3: Optimize Clusters with Principal Component Analysis
Using the original scaled DataFrame, we performed a PCA and reduce the features to three principal components.The total explained variance of the three principal components was 0.895. The first five rows of the PCA DataFrame should appear as follows:

<p align="center">
<img src="https://user-images.githubusercontent.com/118090932/233821199-a32e5ff1-0b6e-45c4-93de-5aeb5051dc80.png" width="400" height="300">
</p>

## Deliverable 4: Find the Best Value for k Using the PCA Data

We used the elbow method on the PCA data to find the best value for k. Based on the below elbow graph, the optimal k-value for clustering is 4.

<p align="center">
<img src="https://user-images.githubusercontent.com/118090932/233821256-c11bf1ca-095a-4be1-863c-d2fba170d2d1.png" width="650" height="400">
</p>

## Deliverable 5: Cluster Cryptocurrencies with K-means Using the PCA Data

We fit the K-Means model using the PCA data, and predicted the clusters to group the cryptocurrencies using the PCA data. The resulting groups are shown in the below scatter plot.

<p align="center">
<img src="https://user-images.githubusercontent.com/118090932/233821323-3119301c-d74c-4d9f-9ab7-ebc66f587502.png" width="600" height="300">
</p>

## Conclusion:
Clustering with PCA reduced inertia. The number of optimal clusters did not change, and grouping stayed similiar. Thus using fewer features did not impact the predicted clusters, showing PCA can be succcessfully used to cluster data while reducing data points used.
