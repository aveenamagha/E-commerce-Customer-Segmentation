# E-commerce Customer Segmentation

# Project Overview

This project focuses on segmenting customers of an e-commerce platform based on their purchase behavior using the K-Means clustering algorithm. The goal is to group customers with similar preferences and behaviors to provide personalized experiences and targeted marketing strategies.

# Problem Statement

E-commerce businesses face challenges in analyzing customer behavior to increase sales and improve customer satisfaction. By clustering customers based on their activity, such as the number of orders placed and the brands they are interested in, businesses can better understand their customers and deliver tailored marketing strategies.

# Dataset Information

The dataset used for this project is collected from an e-commerce platform, containing customer activity data over a specific time period. The dataset includes both customer demographic and behavioral features:

Cust_ID: Unique identifier for each customer.

Gender: Gender of the customer (Male/Female).

Orders: Number of orders placed by each customer.

Brands: Columns representing the number of times a customer has searched for each brand (35 columns).

# Data Preprocessing

Before applying clustering, several preprocessing steps were followed to prepare the data:

Handling Missing Values: Rows with missing values, especially for the 'Gender' column, were dropped to ensure clean data for clustering.

Encoding Categorical Data: The 'Gender' column was one-hot encoded using the pd.get_dummies() function to convert categorical values into numerical form.

Feature Scaling: The numerical features (such as the number of orders and brand searches) were standardized using StandardScaler() to ensure that all features contribute equally to the clustering process.

# Clustering Analysis

Elbow Method for Optimal K

To determine the optimal number of clusters (K), the Elbow Method was used. The Within-Cluster Sum of Squares (WCSS) for different values of K (from 1 to 10) was plotted to visualize the "elbow" point, which indicates the best K value for segmentation.

Silhouette Score

To validate the clustering results, the Silhouette Score was calculated for different K values (from 2 to 9). The silhouette score provides an indication of how well-separated the clusters are. Based on the scores, K=2 was determined as the optimal number of clusters.

Cluster Analysis

The KMeans algorithm was applied with K=2 to segment the customers into two clusters. The clusters were analyzed based on their preferences for different brands, order counts, and other features.

Cluster Distribution

The distribution of customers across the two clusters was visualized using a count plot. Cluster 0 contained 3,042 customers, while Cluster 1 contained 24,234 customers.

# Key Features of Clusters

The cluster centers were analyzed to understand the characteristics of each cluster:

Cluster 0: This cluster consists of customers who have fewer interactions with certain brands, lower order frequency, and exhibit different purchasing behavior compared to Cluster 1.
Cluster 1: This cluster includes customers who have a higher interaction rate with various brands and higher order counts, indicating a more engaged customer base.
Visualizations
Gender Distribution: A pie chart was used to visualize the gender distribution across the customer base.
Cluster Size Distribution: A count plot was used to visualize the number of customers in each cluster.
Numerical Feature Analysis: Boxplots were used to analyze the distribution of order counts and numerical features, highlighting differences between clusters.

# Conclusion

By segmenting customers based on their purchase behavior, businesses can gain valuable insights into customer preferences. The clustering results can guide marketing strategies, product recommendations, and targeted advertising. Further steps could involve analyzing customer loyalty, seasonal trends, or implementing a recommendation system.

# Requirements

Python 3.x

Pandas

Numpy

Matplotlib

Seaborn

Scikit-learn


