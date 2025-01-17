## Cryptocurrency Market Data Clustering with K-means and PCA
# Overview
This project uses K-means clustering and Principal Component Analysis (PCA) to analyze cryptocurrency market data. The dataset contains price change percentages for multiple cryptocurrencies over various timeframes (24h, 7d, 14d, 30d, 60d, 200d, 1y). The objective is to identify clusters of cryptocurrencies based on their price movement patterns over these timeframes.

# Requirements
To run this project, you will need the following Python libraries:

pandas
hvplot
scikit-learn
matplotlib (optional for visualization)

# Data Loading:

The cryptocurrency data is loaded into a Pandas DataFrame using pd.read_csv.

# Data Exploration:

Basic exploratory data analysis (EDA) is performed using describe() and a line plot to visualize the trends in the data.

Data Normalization:

The features are scaled using StandardScaler to standardize the data, making it suitable for clustering.

Elbow Method for Optimal K:

The optimal number of clusters (k) is determined using the elbow method on the scaled data. The inertia (within-cluster sum of squares) for different values of k is plotted to visually identify the best k.

K-means Clustering:

K-means clustering is applied to the scaled data to group the cryptocurrencies into clusters based on their price change percentages over the different timeframes.

Visualization of Clusters:

The resulting clusters are visualized in a scatter plot, with colors representing different clusters.

Principal Component Analysis (PCA):

PCA is applied to reduce the dimensionality of the scaled data to 3 principal components. The explained variance ratio is calculated to determine the amount of information captured by each component.
K-means clustering is applied again to the PCA-reduced data.
Final Clustering and Plotting:

The final clusters are predicted based on the PCA-reduced data, and the results are visualized in a scatter plot.

# Results
Best k Value: Based on the Elbow Curve, the optimal value for k is 4. This value is consistent across both the original and PCA-reduced data.
Cluster Insights: The clusters represent groups of cryptocurrencies with similar price change patterns over time, allowing for better analysis and comparisons.
