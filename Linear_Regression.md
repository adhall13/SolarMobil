# Linear Regression  
Linear regression is a **statistical method** and **machine learning algorithm** (Supervised Machine Learning algorithm) used to model the relationship between a dependent variable (target) and one or more independent variables (predictors) by fitting a straight line to observed data. It estimates the best-fit line to predict future outcomes based on linear relationships. 

## Basic Concepts
3 essential steps:
1. Fit a line to your data
2. Calculate $R^2$ to see how good that fit is
3. Find the p-value to prove the fit

### 1. Fitting the Line (Least Squares)
Find the straight line that best represents the relationship between the independent variable and the dependent variable
* **Residuals**: This is the distance from a specific data point to the regression line
* **Sum of Squared Residuals**: To evaluate a line, measure the residuals for all data points, square each of them, and add them together
* **Least Squares Method**: To find the optimal fit, test different rotations of the line through the data. <br>
The line that results in the lowest (or "least") sum of squared residuals is your final fitted line

### 2. Calculating $R^2$
Once the line is fit, need to determine how useful it is <br>
$R^2$ tells what percentage of the variation in your dependent variable can be explained by taking the independent variable into account <br>
- **Step 1**: Calculate the variation around the simple average (mean) of the data <br>
- **Step 2**: Calculate the variation around the least squares fitted line <br>
- **Formula**: $R^2 = \frac{\text{Variation around the mean} - \text{Variation around the fit}}{\text{Variation around the mean}}$ <br>
- **Adjusted $R^2$**: Adding multiple variables to the equation, your $R^2$ might artificially improve due to random chance. <br>

### 3. Calculating the P-Value for $R^2$
You need a p-value to determine if your $R^2$ is reliable. <br>
For example, if there are only two data points, a perfect line can be drawn between them for an $R^2$ of 100%; it wouldn't mean anything
* **The F-Statistic**: The p-value for $R^2$ is derived from the F-statistic <br>
*The F-statistic* is a value produced by a statistical test (specifically an F-test) that determines whether the relationship between the variables is statistically significant.
In linear regression, it helps you decide if the model’s predictions are actually better than just guessing the average.
* **Formula**: $F = \frac{\text{Variation explained by the fit}}{\text{Variation not explained by the fit}}$ 
* **Degrees of Freedom**: The actual math adjusts the sum of squares into "variances" using degrees of freedom.
This accounts for the sample size and the number of parameters you are trying to estimate <br>
*n|b - sample size (usually denoted as n) is the total number of individual observations or data points included in a specific study or experiment.*
* **Finding the P-Value**: The calculated F-value is plotted onto a standard F-distribution (a curve whose shape is determined by your degrees of freedom).
The p-value represents the probability of achieving that F-value purely by random chance


