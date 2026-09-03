---
id: w02-shushim2-nested-selection
title: "Why Must Selection Be Nested in Cross-Validation?"
author: "Shushi Meng (shushim2)"
---

Suppose we use the full dataset to choose the number of predictors by best-subset selection, and then report 10-fold cross-validation MSE for that already-chosen model. Why is this estimate still optimistic even though each observation is held out once during cross-validation? How would the procedure and interpretation change if best-subset selection were repeated separately inside each training fold? Finally, after nested cross-validation identifies a preferred model size, what data may be used to fit the final model, and why must a truly final test set remain untouched until evaluation?
