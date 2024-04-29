# Linear-Regression

Linear regression is a fundamental statistical method used for predicting the value of a continuous variable based on one or more input features. It assumes a linear relationship between the input features and the output variable. Here are the key aspects of linear regression:

1. **Model Representation**:
   - Linear regression models the relationship between the input variables (\(x\)) and the output variable (\(y\)) as a linear equation:
     \[ y = \theta_0 + \theta_1 x_1 + \theta_2 x_2 + \ldots + \theta_n x_n \]
   - Here, \(y\) is the predicted output, \(\theta_0, \theta_1, \ldots, \theta_n\) are the coefficients (also called weights or parameters) to be learned, and \(x_1, x_2, \ldots, x_n\) are the input features.

2. **Training**:
   - During the training phase, the goal is to learn the coefficients (\(\theta\)) that minimize the difference between the predicted values and the actual values in the training data.
   - This is typically achieved by minimizing a loss function such as mean squared error (MSE) or mean absolute error (MAE) using optimization techniques like ordinary least squares (OLS) or gradient descent.

3. **Interpretation**:
   - The coefficients (\(\theta\)) in linear regression represent the change in the output variable for a one-unit change in the corresponding input variable, assuming all other variables are held constant.
   - For example, if \(\theta_1\) is the coefficient for \(x_1\), then an increase of one unit in \(x_1\) results in a change of \(\theta_1\) units in the predicted value of \(y\), holding all other variables constant.

4. **Assumptions**:
   - Linear regression makes several assumptions about the data, including linearity (the relationship between the input and output is linear), independence of errors (the errors are not correlated with each other), and homoscedasticity (constant variance of errors).

5. **Use Cases**:
   - Linear regression is commonly used for various prediction tasks, such as predicting house prices based on features like size, number of bedrooms, etc., forecasting sales based on advertising spending, and predicting exam scores based on study time.

6. **Extensions**:
   - There are extensions of linear regression, such as polynomial regression (where the relationship between the variables is modeled as an nth degree polynomial) and multiple linear regression (where there are multiple input features).

Linear regression is a simple yet powerful tool for understanding and making predictions based on data with a linear relationship between the input features and the output variable.
