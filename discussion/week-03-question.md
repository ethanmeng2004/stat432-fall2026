---
id: w03-shushim2-ridge-units
title: "Should Changing Units Change a Ridge Model?"
author: "Shushi Meng (shushim2)"
---

Suppose two students fit the same ridge regression model for house prices using floor area and age. One records area in square feet, while the other records the same values in thousands of square feet. In ordinary least squares, the area coefficient simply rescales, so the fitted values do not change. With the same value of $\lambda$, however, ridge regression may produce different fitted values because it penalizes the squared numerical sizes of the coefficients.

Should a change of measurement units be able to change the model's predictions? Explain how standardizing the predictors makes the ridge penalty more comparable across variables. In the same spirit, why is the intercept usually left unpenalized, and what unwanted effect could occur if it were shrunk toward zero along with the other coefficients?
