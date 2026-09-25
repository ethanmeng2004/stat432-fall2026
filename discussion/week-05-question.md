---
id: w05-shushim2-redundant-knn
title: "Can Redundant Predictors Distort KNN?"
author: "Shushi Meng (shushim2)"
---

Suppose a KNN classifier predicts loan default using standardized income, age, and five nearly identical measures of credit utilization. Although the five utilization variables contain almost the same information, each contributes separately to Euclidean distance. How could this redundancy change which observations are selected as nearest neighbors compared with using only one utilization measure? Would standardizing the predictors solve the problem, or would it leave the repeated information overweighted? What preprocessing or variable-selection strategies could reduce this distortion, and what trade-offs might arise if the correlated variables contain slightly different nonlinear predictive information?
