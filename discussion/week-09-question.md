---
id: w09-shushim2-svm-kernel-selection
title: "When Is a Nonlinear SVM Worth the Complexity?"
author: "Shushi Meng (shushim2)"
---

Suppose we compare a linear SVM with a radial-kernel SVM using the same cross-validation folds and standardize the predictors within each training fold. After tuning $C$ for both models and $\gamma$ for the radial model, the radial SVM has a slightly lower mean validation error. Is that small improvement enough to justify choosing the nonlinear model? How could variation across folds and sensitivity to nearby tuning settings help us decide whether the improvement is reliable, and how should we estimate the selected model's performance without reusing the results that guided tuning?
