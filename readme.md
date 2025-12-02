## 1. Overall Model Assessment (The $R^2$ and F-Test) 📊

This section assesses how well your entire set of predictors collectively explains the variation in the restaurant `rating`.

### Statistic,Interpretation,Significance in Project

- F-statistic,Tests the overall significance of the model:
"If the associated P-value (e.g., P<2.2e−16 or P<0.001) is less than α=0.05, the model is statistically significant. We reject the null hypothesis that all predictor coefficients are zero."

- R2 (Multiple R-squared),The proportion of the total variation in rating that is explained by all the predictor variables together.:
"An R2 of, for example, 0.468 means 46.8% of the variability in ratings is explained by your combined features (review count, price, service types, and restaurant type)."

- Adjusted R2,A modified R2 that accounts for the number of predictors in the model:
"This is a better measure for comparison, as it penalizes models for including irrelevant variables. If the Adjusted R2 is much lower than R2, it confirms that many of your predictors (likely the numerous primaryType dummy variables) are not useful and the model is slightly overfit."


### Column,Interpretation

- Estimate (Coefficient β),"The estimated change in the mean rating for a one-unit increase in the predictor, holding all other variables constant."

- Std. Error,Measures the precision of the coefficient estimate. A smaller Standard Error means the estimate is more precise.

- t value,The test statistic for the individual predictor. Measures the number of standard errors the coefficient is away from zero.

- **Pr(>,t

## 3. Residuals (The Error Distribution)

The top section of the output shows a five-number summary (Min, 1Q, Median, 3Q, Max) of the model's residuals (the prediction errors: $Y - \hat{Y}$).

### Statistic,Interpretation

- Median,"Should be close to zero. If the median is far from zero, it suggests the model is systematically biased (e.g., over- or under-predicting)."

- Min & Max,Indicate the size of the largest errors. Extremely large positive or negative values suggest outliers or heteroscedasticity.

- 1Q & 3Q,Show the spread of the middle 50% of the errors. These should be relatively symmetric around zero.
