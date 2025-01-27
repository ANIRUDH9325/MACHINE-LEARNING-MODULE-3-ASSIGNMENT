**Answers to the Regression Assignment Questions**

### 1. **What is Simple Linear Regression?**
Simple Linear Regression is a statistical method used to model the relationship between a dependent variable (“Y”) and a single independent variable (“X”). It fits a straight line to the data using the equation:

\[
Y = mX + c
\]

Where:
- \(m\) is the slope (rate of change of \(Y\) with respect to \(X\)).
- \(c\) is the intercept (value of \(Y\) when \(X = 0\)).

### 2. **What are the key assumptions of Simple Linear Regression?**
- **Linearity**: The relationship between the independent and dependent variables is linear.
- **Independence**: Observations are independent of each other.
- **Homoscedasticity**: The variance of residuals is constant across all levels of \(X\).
- **Normality**: The residuals (errors) are normally distributed.

### 3. **What does the coefficient \(m\) represent in the equation \(Y = mX + c\)?**
The coefficient \(m\) represents the slope of the regression line. It indicates the rate of change in the dependent variable \(Y\) for a one-unit increase in the independent variable \(X\).

### 4. **What does the intercept \(c\) represent in the equation \(Y = mX + c\)?**
The intercept \(c\) represents the value of the dependent variable \(Y\) when the independent variable \(X = 0\). It’s where the regression line crosses the \(Y\)-axis.

### 5. **How do we calculate the slope \(m\) in Simple Linear Regression?**
The slope \(m\) is calculated using the formula:

\[
m = \frac{\sum{(X_i - \bar{X})(Y_i - \bar{Y})}}{\sum{(X_i - \bar{X})^2}}
\]

Where:
- \(X_i\) and \(Y_i\) are individual data points.
-  \(\bar{X}\) and \(\bar{Y}\) are the means of \(X\) and \(Y\), respectively.

### 6. **What is the purpose of the least squares method in Simple Linear Regression?**
The least squares method minimizes the sum of the squared differences between the observed values and the predicted values. It ensures the best-fitting line has the smallest possible error.

### 7. **How is the coefficient of determination (\(R^2\)) interpreted in Simple Linear Regression?**
The coefficient of determination (\(R^2\)) measures how much of the variability in the dependent variable \(Y\) is explained by the independent variable \(X\). It ranges from 0 to 1:
- \(R^2 = 1\): Perfect fit.
- \(R^2 = 0\): No relationship.

---

### 8. **What is Multiple Linear Regression?**
Multiple Linear Regression is an extension of Simple Linear Regression where two or more independent variables (\(X_1, X_2, …, X_n\)) are used to predict the dependent variable (\(Y\)). The equation is:

\[
Y = b_0 + b_1X_1 + b_2X_2 + … + b_nX_n
\]

Where:
- \(b_0\) is the intercept.
- \(b_1, b_2, …, b_n\) are the coefficients for each independent variable.

### 9. **What is the main difference between Simple and Multiple Linear Regression?**
- **Simple Linear Regression**: Involves one independent variable.
- **Multiple Linear Regression**: Involves two or more independent variables.

### 10. **What are the key assumptions of Multiple Linear Regression?**
- **Linearity**: The relationship between independent variables and \(Y\) is linear.
- **Independence**: Observations are independent.
- **Homoscedasticity**: Constant variance of residuals.
- **Normality**: Residuals are normally distributed.
- **No Multicollinearity**: Independent variables are not highly correlated.

### 11. **What is heteroscedasticity, and how does it affect the results of a Multiple Linear Regression model?**
Heteroscedasticity occurs when the variance of residuals is not constant across all levels of the independent variables. It can lead to:
- Biased standard errors.
- Inefficient estimators.
- Misleading hypothesis test results.

### 12. **How can you improve a Multiple Linear Regression model with high multicollinearity?**
- Remove or combine highly correlated variables.
- Use techniques like Principal Component Analysis (PCA).
- Regularization methods (e.g., Lasso or Ridge regression).

### 13. **What are some common techniques for transforming categorical variables for use in regression models?**
- **One-Hot Encoding**: Converts categories into binary columns.
- **Label Encoding**: Assigns numeric labels to categories.
- **Dummy Variables**: Creates binary variables for each category, excluding one to avoid multicollinearity.

### 14. **What is the role of interaction terms in Multiple Linear Regression?**
Interaction terms allow modeling the combined effect of two independent variables on the dependent variable. For example:

\[
Y = b_0 + b_1X_1 + b_2X_2 + b_3(X_1 \times X_2)
\]

Here, \(b_3\) measures how the effect of \(X_1\) changes with \(X_2\).

### 15. **How can the interpretation of intercept differ between Simple and Multiple Linear Regression?**
In **Simple Linear Regression**, the intercept is the value of \(Y\) when \(X = 0\). In **Multiple Linear Regression**, the intercept is the value of \(Y\) when all independent variables are 0, which might not always be meaningful.

### 16. **What is the significance of the slope in regression analysis, and how does it affect predictions?**
The slope represents the rate of change of the dependent variable (\(Y\)) for a one-unit increase in the independent variable (\(X\)). It helps in understanding and predicting the relationship between variables.

### 17. **How does the intercept in a regression model provide context for the relationship between variables?**
The intercept provides the baseline value of \(Y\) when all independent variables are 0. It helps in contextualizing predictions and understanding the starting point of the relationship.

### 18. **What are the limitations of using \(R^2\) as a sole measure of model performance?**
- Does not indicate whether the model is appropriate.
- Can be artificially high with more independent variables.
- Does not account for overfitting.
- Does not provide information on the magnitude or direction of errors.

### 19. **How would you interpret a large standard error for a regression coefficient?**
A large standard error indicates that the estimate for the regression coefficient is imprecise. This can result from:
- High multicollinearity.
- Small sample size.
- Outliers in the data.

### 20. **How can heteroscedasticity be identified in residual plots, and why is it important to address it?**
- Identified by plotting residuals vs. predicted values: A funnel-shaped pattern indicates heteroscedasticity.
- Addressing it is important to avoid biased standard errors and unreliable hypothesis tests.

### 21. **What does it mean if a Multiple Linear Regression model has a high \(R^2\) but low adjusted \(R^2\)?**
This indicates that additional variables in the model are not contributing meaningfully to explaining the variance in \(Y\). Adjusted \(R^2\) penalizes the addition of non-significant variables.

### 22. **Why is it important to scale variables in Multiple Linear Regression?**
- To ensure that all variables contribute equally to the model.
- To improve numerical stability and convergence of optimization algorithms.

---

### Polynomial Regression Questions

### 23. **What is polynomial regression?**
Polynomial regression is a type of regression analysis where the relationship between the independent variable \(X\) and dependent variable \(Y\) is modeled as an \(n\)-degree polynomial.

### 24. **How does polynomial regression differ from linear regression?**
- **Linear Regression**: Models a straight-line relationship.
- **Polynomial Regression**: Models a curved relationship using higher-degree terms (e.g., \(X^2, X^3\)).

### 25. **When is polynomial regression used?**
Used when the data shows a non-linear relationship that cannot be captured by a straight line.

### 26. **What is the general equation for polynomial regression?**
\[
Y = b_0 + b_1X + b_2X^2 + … + b_nX^n
\]

### 27. **Can polynomial regression be applied to multiple variables?**
Yes, it can be extended to multiple variables by including polynomial terms of each variable and their interactions.

### 28. **What are the limitations of polynomial regression?**
- Risk of overfitting with high-degree polynomials.
- Sensitive to outliers.
- Can become computationally expensive for large datasets.

### 29. **What methods can be used to evaluate model fit when selecting the degree of a polynomial?**
- Cross-validation.
- Comparing \(R^2\) and Adjusted \(R^2\).
- Residual analysis.

### 30. **Why is visualization important in polynomial regression?**
Visualization helps in understanding the data’s shape and how well the polynomial curve fits the data points.

### 31. **How is polynomial regression implemented in Python?**
Using libraries like `scikit-learn`:

```python
from sklearn.preprocessing import PolynomialFeatures
from sklearn.linear_model import LinearRegression
from sklearn.pipeline import Pipeline

# Create a pipeline for polynomial regression
model = Pipeline([
    ("poly_features", PolynomialFeatures(degree=2)),
    ("linear_regression", LinearRegression())
])

# Fit the model
model.fit(X, y)
```

