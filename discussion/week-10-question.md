---
id: w10-shushim2-forest-feature-subsampling
title: "When Can Less Feature Subsampling Help a Random Forest?"
author: "Shushi Meng (shushim2)"
---

Suppose a classification dataset has one strong predictor and many weak predictors. We fit two random forests with the same number of trees and the same tree-size settings, but one considers fewer candidate predictors at each split. Using fewer candidates may make the trees less similar, yet it may also prevent many splits from using the strong predictor. Under what conditions would you expect this change to improve or worsen prediction on new data? How could out-of-bag error help us choose the number of candidate predictors, and why might simply adding more trees fail to compensate for a poor choice?
