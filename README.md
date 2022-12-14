# Silhouette_Clustering_Analysis
A technique to validate the decided number clusters in clustering algorithms are correct or not

Wiki:- https://en.wikipedia.org/wiki/Silhouette_(clustering)#:~:text=The%20silhouette%20value%20is%20a,poorly%20matched%20to%20neighboring%20clusters

sklearn:- https://scikit-learn.org/stable/auto_examples/cluster/plot_kmeans_silhouette_analysis.html#sphx-glr-auto-examples-cluster-plot-kmeans-silhouette-analysis-py

Silhouette analysis can be used to study the separation distance between the resulting clusters. The silhouette plot displays a measure of how close each point in one cluster is to points in the neighboring clusters and thus provides a way to assess parameters like number of clusters visually. This measure has a range of [-1, 1].

Silhouette coefficients (as these values are referred to as) near +1 indicate that the sample is far away from the neighboring clusters. A value of 0 indicates that the sample is on or very close to the decision boundary between two neighboring clusters and negative values indicate that those samples might have been assigned to the wrong cluster.

In this example the silhouette analysis is used to choose an optimal value for n_clusters. The silhouette plot shows that the n_clusters value of 3, 5 and 6 are a bad pick for the given data due to the presence of clusters with below average silhouette scores and also due to wide fluctuations in the size of the silhouette plots. Silhouette analysis is more ambivalent in deciding between 2 and 4.

Also from the thickness of the silhouette plot the cluster size can be visualized. The silhouette plot for cluster 0 when n_clusters is equal to 2, is bigger in size owing to the grouping of the 3 sub clusters into one big cluster. However when the n_clusters is equal to 4, all the plots are more or less of similar thickness and hence are of similar sizes as can be also verified from the labelled scatter plot on the right.

![image](https://user-images.githubusercontent.com/98344033/200975836-88a05e4d-f62e-456c-8672-7fa236bed03a.png)

![image](https://user-images.githubusercontent.com/98344033/200975941-2960de1f-4259-406b-b733-a5adf10f6ddd.png)

![image](https://user-images.githubusercontent.com/98344033/200975969-6993fdc8-2782-4a15-bfec-377395209553.png)

![image](https://user-images.githubusercontent.com/98344033/200975983-60796b5f-36c9-4a24-a1aa-a4d2a3a799d1.png)

![image](https://user-images.githubusercontent.com/98344033/200976001-fa3fd704-5b41-4393-83ba-1f375c118a4f.png)


For n_clusters = 2 The average silhouette_score is : 0.7049787496083262

For n_clusters = 3 The average silhouette_score is : 0.5882004012129721

For n_clusters = 4 The average silhouette_score is : 0.6505186632729437

For n_clusters = 5 The average silhouette_score is : 0.56376469026194

For n_clusters = 6 The average silhouette_score is : 0.4504666294372765
