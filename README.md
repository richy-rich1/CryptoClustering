# Cryptocurrency Clustering Project

This project uses clustering techniques to analyze and group cryptocurrencies based on their market data. By leveraging k-means clustering and Principal Component Analysis (PCA), the project identifies patterns and insights within the cryptocurrency market.

## Project Workflow

### 1. Rename the File
- Rename `Crypto_Clustering_starter_code.ipynb` to `Crypto_Clustering.ipynb`.

### 2. Load and Explore the Data
- Load the dataset `crypto_market_data.csv` into a Pandas DataFrame.
- Perform exploratory data analysis (EDA):
  - Display summary statistics.
  - Visualize the data distributions.

### 3. Data Preprocessing
- Normalize the dataset using the `StandardScaler` module from scikit-learn.
- Create a new DataFrame with scaled data and set the `coin_id` column as the index.

### 4. Finding the Best Value for k (Elbow Method)
- Use the elbow method to identify the optimal number of clusters (k):
  - Create a range of k values (1 to 11).
  - Calculate the inertia for each k value.
  - Plot the elbow curve to visually determine the best k.

### 5. K-Means Clustering
- Perform k-means clustering using the optimal k value on the scaled dataset.
- Add a `cluster` column to the DataFrame to store the cluster assignments.
- Visualize the clusters using an interactive scatter plot (hvPlot):
  - X-axis: `price_change_percentage_24h`
  - Y-axis: `price_change_percentage_7d`
  - Hover information: `coin_id`

### 6. Principal Component Analysis (PCA)
- Reduce the features to 3 principal components using PCA.
- Retrieve the explained variance to measure information captured by the components.
- Create a new DataFrame with the PCA-transformed data and retain the `coin_id` index.

### 7. Finding the Best Value for k with PCA
- Use the elbow method on the PCA DataFrame to find the optimal k value.
- Compare the k value derived from PCA data to the one derived from the original scaled data.

### 8. K-Means Clustering with PCA
- Perform k-means clustering on the PCA DataFrame using the optimal k value.
- Add a `cluster` column to the PCA DataFrame to store the cluster assignments.
- Visualize the PCA clusters using an interactive scatter plot (hvPlot):
  - X-axis: `PC1`
  - Y-axis: `PC2`
  - Hover information: `coin_id`

### 9. Analysis and Insights
- Analyze and compare the results of clustering with and without PCA.
- Reflect on the impact of dimensionality reduction on clustering accuracy and interpretability.

## Files
- `crypto_market_data.csv`: The dataset containing cryptocurrency market data.
- `Crypto_Clustering.ipynb`: The Jupyter Notebook with code and analysis.

## Requirements
The following Python libraries are required to run this project:
- pandas
- matplotlib
- scikit-learn
- hvplot
- numpy

Install these dependencies using:
```bash
pip install pandas matplotlib scikit-learn hvplot numpy
```

