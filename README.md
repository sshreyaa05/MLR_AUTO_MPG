### Multiple Linear Regression Project Using Auto MPG Data Leveraging the Ordinary Least Squares Estimation
### Objective:
This project applies Multiple Linear Regression to predict Miles per Gallon (MPG) based on various car features using the Auto MPG dataset from the Seaborn library. The analysis includes preprocessing, model fitting using OLS (Ordinary Least Squares), and evaluating model parameters for significance and multicollinearity.
### 1. Data Preprocessing:
The dataset was first loaded directly from Seaborn.
Missing values were handled by dropping rows with missing values.
Label Encoding was applied to convert categorical variables into numerical format to make them suitable for the regression model.
### 2. Model Fitting:
OLS Estimation was used to fit the model using Statsmodels API.
The dependent variable was MPG, and the independent variables included features such as Cylinders, Displacement, Horsepower, Weight, Acceleration, Model Year, and Origin.
### 3. Parameter Estimation:
Estimated parameters included:
Bias (intercept) of the regression equation.
Regression Coefficients for each independent variable.
Error Variance to assess the model’s fit.
### 4. Confidence Intervals and Significance Testing:
Confidence Intervals for the parameters were calculated to assess the precision of the regression coefficients.
Partial Regression Coefficients were tested for statistical significance to determine which variables have a significant impact on predicting MPG, therefore, variables with p-values less than 0.05 (such as cylinders, displacement, weight, model_year and origin) are statistically significant and have a meaningful impact on MPG, whereas, Horsepower and acceleration are not significant, indicating their contribution to predicting MPG is likely minimal in this model.
### 5. Multicollinearity Detection:
a. Correlation Matrix: Strong correlations exist between Cylinders, Displacement, and Weight, with values above 0.85. This suggests potential multicollinearity between these predictors. Acceleration and Horsepower show negative correlations with Cylinders and Weight, respectively, which could indicate inverse relationships between certain features.

b. Variance Inflation Factor (VIF): VIF values for Displacement (20.64) and Horsepower (9.92) are high, indicating potential multicollinearity. The VIF for Cylinders (8.39) is also relatively high, suggesting redundancy with other features like Displacement and Weight. VIF for Acceleration (2.62) and Model Year (1.29) are lower, indicating these variables are less affected by multicollinearity. Model Year and Origin have VIFs of around 1.29 and 1.71, respectively, suggesting minimal collinearity issues for these predictors.

c. Condition Number: The Condition Number is extremely large (45,828,228.98), indicating severe multicollinearity in the dataset. This high condition number suggests that the model might be unstable and sensitive to small changes in the data, which could distort the regression results.
### 6. Condition Indices:
The Condition Indices range from 1.0 to 45,828,229, with the largest values occurring for Cylinders and Displacement. These indices confirm that multicollinearity is a significant issue, especially for these highly correlated variables.
### 7. Model Adequacy:
a. R-Squared (0.8239) indicates that the model explains 82.4% of the variance in MPG, which is a good fit.
b. Adjusted R-Squared (0.8207) shows the model is not overfitting, with only a slight reduction from the R-Squared value, which is typical for a model with multiple predictors.


