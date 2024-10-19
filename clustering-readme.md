# Unsupervised Learning - Clustering Analysis Project

## Overview
This project implements various clustering algorithms to perform unsupervised learning on datasets. It includes implementation of K-means, DBSCAN, and Hierarchical clustering algorithms, along with evaluation metrics and visualization capabilities.

## Features
- Multiple clustering algorithms:
  - K-means clustering
  - DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
  - Hierarchical clustering (Agglomerative)
- Automated data preprocessing and scaling
- Clustering evaluation metrics:
  - Silhouette Score
  - Davies-Bouldin Index
- Visual representation of clustering results
- Synthetic dataset generation for testing

## Requirements
- Python 3.7+
- Required packages:
  ```
  numpy
  pandas
  matplotlib
  scikit-learn
  seaborn
  ```

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/clustering-analysis.git
   cd clustering-analysis
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. Basic usage:
   ```python
   from clustering_analysis import ClusteringAnalysis
   
   # Initialize with default parameters
   analyzer = ClusteringAnalysis()
   
   # Run complete analysis
   analyzer.run_analysis()
   ```

2. Custom parameters:
   ```python
   # Initialize with custom parameters
   analyzer = ClusteringAnalysis(
       n_samples=500,       # Number of data points
       n_features=2,        # Number of features
       n_clusters=4,        # Number of clusters
       random_state=42      # Random seed for reproducibility
   )
   
   # Run specific clustering algorithm
   kmeans_labels, kmeans_model = analyzer.perform_kmeans(n_clusters=4)
   dbscan_labels = analyzer.perform_dbscan(eps=0.3, min_samples=5)
   ```

## Configuration Options
- `n_samples`: Number of data points to generate (default: 300)
- `n_features`: Number of features in the dataset (default: 2)
- `n_clusters`: Number of clusters to generate/find (default: 3)
- `random_state`: Random seed for reproducibility (default: 42)

### Clustering Parameters
#### K-means
- `n_clusters`: Number of clusters (default: 3)

#### DBSCAN
- `eps`: Maximum distance between samples (default: 0.3)
- `min_samples`: Minimum number of samples in a neighborhood (default: 5)

#### Hierarchical Clustering
- `n_clusters`: Number of clusters (default: 3)

## Output
The analysis provides:
1. Numerical evaluation metrics:
   - Silhouette Score (ranges from -1 to 1, higher is better)
   - Davies-Bouldin Index (lower is better)
2. Visualizations:
   - Scatter plots of clustered data
   - Color-coded cluster assignments

## Example Output
```
Clustering Evaluation Metrics:
----------------------------------------

K-means Clustering:
Silhouette Score: 0.823
Davies-Bouldin Index: 0.524

DBSCAN Clustering:
Silhouette Score: 0.756
Davies-Bouldin Index: 0.687

Hierarchical Clustering:
Silhouette Score: 0.801
Davies-Bouldin Index: 0.548
```

## Contributing
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Future Improvements
- Add more clustering algorithms (e.g., OPTICS, Mean-shift)
- Implement automatic parameter tuning
- Add support for categorical data
- Include more evaluation metrics
- Add interactive visualizations
- Support for high-dimensional data visualization

## Contact
Your Name - [your.email@example.com](mailto:your.email@example.com)
Project Link: [https://github.com/yourusername/clustering-analysis](https://github.com/yourusername/clustering-analysis)

## Acknowledgments
- scikit-learn documentation and community
- Python data science community
- List any other resources or inspirations
