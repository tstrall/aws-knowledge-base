# Regression Metrics in Machine Learning

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Machine Learning – Specialty (MLS)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

Regression metrics are quantitative measures used to evaluate the performance of machine learning models that predict continuous outcomes. They assess the accuracy of predicted values against actual values, guiding model selection, tuning, and deployment decisions.

---

## Why should I care?

- **Performance Assessment**: Understand how well your model predicts continuous data.
- **Model Comparison**: Compare different models to select the most accurate one.
- **Error Analysis**: Identify and quantify prediction errors to improve model performance.
- **Business Impact**: Ensure that model predictions meet business accuracy requirements.

---

## Key Metrics

### 1. Mean Absolute Error (MAE)

- **Definition**: The average of absolute differences between predicted and actual values.
- **Formula**: MAE = (1/n) * Σ|yᵢ - ŷᵢ|
- **Use Case**: Provides a straightforward interpretation of average error magnitude.

### 2. Mean Squared Error (MSE)

- **Definition**: The average of squared differences between predicted and actual values.
- **Formula**: MSE = (1/n) * Σ(yᵢ - ŷᵢ)²
- **Use Case**: Penalizes larger errors more than MAE, useful when large errors are particularly undesirable.

### 3. Root Mean Squared Error (RMSE)

- **Definition**: The square root of the mean squared error.
- **Formula**: RMSE = √MSE
- **Use Case**: Expresses error in the same units as the target variable, making interpretation easier.

### 4. R-squared (Coefficient of Determination)

- **Definition**: Measures the proportion of variance in the dependent variable predictable from the independent variables.
- **Formula**: R² = 1 - (SS_res / SS_tot)
- **Use Case**: Indicates the goodness of fit; values closer to 1 signify better fit.

### 5. Adjusted R-squared

- **Definition**: Adjusts the R-squared value based on the number of predictors, preventing overestimation with multiple variables.
- **Use Case**: Useful when comparing models with different numbers of predictors.

### 6. Mean Absolute Percentage Error (MAPE)

- **Definition**: The average of absolute percentage errors between predicted and actual values.
- **Formula**: MAPE = (1/n) * Σ(|(yᵢ - ŷᵢ) / yᵢ|) * 100%
- **Use Case**: Expresses error as a percentage, making it intuitive for business contexts.

### 7. Root Mean Squared Logarithmic Error (RMSLE)

- **Definition**: Measures the ratio between the true and predicted values, focusing on the relative error.
- **Formula**: RMSLE = √[(1/n) * Σ(log(ŷᵢ + 1) - log(yᵢ + 1))²]
- **Use Case**: Useful when the target variable spans several orders of magnitude.

---

## When to use which metric?

- **MAE**: When all errors are equally important.
- **MSE/RMSE**: When larger errors are more significant and should be penalized.
- **R-squared/Adjusted R-squared**: To assess the proportion of variance explained by the model.
- **MAPE**: When expressing errors as percentages is more interpretable.
- **RMSLE**: When dealing with exponential growth or targets with large ranges.

---

## Learn More

- [Regression Metrics for Machine Learning](https://www.machinelearningmastery.com/regression-metrics-for-machine-learning/)
- [A Comprehensive Overview of Regression Evaluation Metrics](https://developer.nvidia.com/blog/a-comprehensive-overview-of-regression-evaluation-metrics/)
- [Know The Best Evaluation Metrics for Your Regression Model](https://www.analyticsvidhya.com/blog/2021/05/know-the-best-evaluation-metrics-for-your-regression-model/)
