# Introduction
Welcome to the Clustering Wine DataSet wiki!
The objective of this analysis is to apply clustering algorithms, namely K-means and Agglomerative Hierarchical Clustering (AHC), to partition the dataset into groups based on similarities. The dataset is available on Kaggle. It consists of six classes. 

# K-Means and Agglomerative Hierarchical Clustering
K-means is a partitional clustering algorithm that partitions a set of vectors into _k_ clusters through exploratory data analysis (Jeong et al., 2018; Ali Moez, 2022; Zalik, 2008; Zoumana Keita, 2023). On the other hand, Agglomerative Hierarchical Clustering works by iteratively creating clusters based on the similarities of attributes until the final cluster is formed (Zoumana Keita, 2023).

# Pre-processing and scores
Both datasets were scaled using Standard Scaler and Robust Scaler techniques. Their silhouette and ARI scores were determined.
Silhouette Score ranges from -1 to 1, where a higher value indicates better-defined and well-separated clusters. ARI ranges from -1 to 1, where a value close to 1 indicates a strong agreement, a value close to 0 indicates random labelling, and a value close to -1 indicates a strong disagreement. 

For the features scaled using Standard Scaler, the K-means and AHC models achieved a silhouette score of 0.205 and 0.206, respectively. The ARI scores for these models were 0.034 and 0.026, respectively.

For the features scaled using Robust Scaler, the K-means and AHC models achieved a higher silhouette score of 0.717 and 0.75, respectively. However, the ARI scores for these models were -0.003 and -0.002, respectively.

Both K-means and Agglomerative Hierarchical Clustering algorithms were visualized using Scatter plots for K-means and dendrograms. The Scatter plot provides a visual representation of the clusters formed by K-means while dendrogram on the other hand illustrates the hierarchical structure of clusters in AHC. These images are provided below.

![Kmeans-scaled](https://github.com/temmyfioye/ClusteringWineDataSet/assets/26744249/55d9c7ef-2e52-46b0-86d8-4ef4738fc868)
![AHC-Robust (1)](https://github.com/temmyfioye/ClusteringWineDataSet/assets/26744249/f6803e3c-9c98-4ea3-946a-ba3f0275bc82)

# Discussion and conclusion
These scores provide an evaluation of the performance of the clustering algorithms on the dataset, with higher silhouette scores indicating better separation and cohesion of the clusters. The ARI scores indicate the agreement between the clustering results and the true labels, with values closer to 1 indicating better agreement.
For both the K-means and AHC models, it is observed that the features scaled using the Robust Scaler performed better in terms of silhouette scores, indicating improved separation and cohesion of the clusters. On the other hand, the features scaled using the Standard Scaler performed better in terms of the ARI, indicating a higher agreement between the clustering results and the true labels.

This suggests that the choice of scaling technique can impact the performance of the clustering algorithms. The Robust Scaler, which is more resilient to outliers, resulted in higher silhouette scores, suggesting better-defined clusters. However, in terms of ARI, the Standard Scaler, which assumes a Gaussian distribution, yielded better agreement with the true labels.

It is important to consider the characteristics of the dataset and the specific requirements of the analysis when selecting the scaling technique. Different scaling methods may have varying effects on the clustering results, and the choice should be made based on the specific data and clustering objectives.

# References
* Ali Moez, 2022. Clustering in Machine Learning: 5 Essential Clustering Algorithms [online]. Available at: https://www.datacamp.com/blog/clustering-in-machine-learning-5-essential-clustering-algorithms
* Jeong, Y., Lee, J., Moon, J., Shin, J.H. and Lu, W.D., 2018. K‑means Data Clustering with Memristor Networks. Nano Letters; Nano Lett, 18 (7), 4447-4453.
* Zalik, K.R., 2008. An efficient k′-means clustering algorithm. Pattern Recognition Letters, 29 (9), 1385-1391.
* Zoumana Keita, 2023. An Introduction to Hierarchical Clustering in Python [online]. Available at: https://www.datacamp.com/tutorial/introduction-hierarchical-clustering-python.

