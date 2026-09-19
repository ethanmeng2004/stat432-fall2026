---
id: w04-shushim2-correlated-lasso
title: "Can Lasso Selection Be Unstable?"
author: "Shushi Meng (shushim2)"
---

Suppose two predictors, $X_1$ and $X_2$, are highly correlated and contain nearly the same information about the response. A lasso model fitted on one training sample selects $X_1$ and sets the coefficient of $X_2$ to zero, while a model fitted on a slightly different sample—or with a nearby value of $\lambda$—selects $X_2$ instead. Despite this change, the two models have almost the same cross-validation prediction error.

Why can lasso's selected variables be unstable even when its predictions are stable? In this situation, should we interpret the selected variable as uniquely important? What additional evidence or modeling approach could help us assess whether the conclusion is reliable?
