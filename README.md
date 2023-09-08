# Multilinear Regression - Store Sales

## Question
What factors are most important for determining the annual sales for men's clothing stores in the Netherlands?

## Data
A cross section of Men's Fashion stores in the Netherlands from 1990. The dataset contains 400 observations.

Features:
* `tsales`: annual sales in Dutch guilders
* `sales`: sales per square meter
* `margin`: gross-profit-margin
* `nown`: number of owners (managers)
* `nfull`: number of full-timers
* `npart`: number of part-timers
* `naux`: number of helpers (temporary workers)
* `hoursw`: total number of hours worked
* `hourspw`: number of hours worked per worker
* `inv1`: investment in shop-premises
* `inv2`: investment in automation.
* `ssize`: sales floor space of the store (in m^2).
* `start`: year start of business

## Analysis
Initial analysis only included `tsales`, `margin`, `nown`, `inv1`, `inv2`, `ssize`, and `start`, as these features seemed most relevant.

Summary statistics were generated and a correlation matrix was created to check for possible collinearity issues.<br>
![image](https://github.com/nwferreri/multilinear-regression/assets/112211174/cca818f8-e5bd-40e4-b8ca-28412fd01870)<br>
No significant collinearity was found, so analysis proceeded with selected variables.

A model was generated using Ordinary Least Squares (OLS) and showed that `ssize` and possibly `margin` were the only statistically significant features.

A second model was run using only those features, but showed no significant improvement.

## Evaluation
Both mean absolute error (MAE) and root mean squared error (RMSE) were calculated. They indicated that the model may be strongly affected by outliers. The errors were deemed acceptable.

## Conclusions
Analysis suggests that the sales floor space of the store is the most statistically significant predictor of annual sales.
