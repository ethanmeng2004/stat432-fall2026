---
id: w08-shushim2-svm-outlier-cost
title: "How Should an SVM Respond to an Outlier?"
author: "Shushi Meng (shushim2)"
---

Suppose a linear SVM has one training observation far from the rest of its class, near the opposite class. Increasing the cost parameter could make the model work harder to classify that point correctly, but might also narrow the margin and shift the boundary for many other observations. How would you decide whether that point should strongly influence the boundary? What patterns in cross-validation results or support vectors would help you tell whether a larger cost is improving generalization or mainly fitting the unusual observation?
