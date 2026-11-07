---
id: w11-shushim2-pca-clustering-information
title: "Can PCA Hide Meaningful Clusters?"
author: "Shushi Meng (shushim2)"
---

Suppose we standardize the variables in a dataset and apply PCA before K-means clustering. The first two principal components explain 90% of the total variance, but a direction with little variance may separate meaningful groups. Would retaining only the first two components necessarily lead to useful clusters? How could we compare clustering results across different numbers of retained components to check whether PCA has removed important grouping information, and why would comparing only the within-cluster sum of squares across these different representations be misleading?
