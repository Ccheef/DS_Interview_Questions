**1. What are the main assumptions of linear regression? What are the most common types of linear regression (most common estimation techniques)?**
* The two main assumptions: 1. The relationship between independent variable X and dependent variable Y should be linear. 2. The residual errors from the regression fit should be normally distributed. 
* The common types: 1. Ordinary Least Squares 2. Generalized Least Squares ([see OLS and GLS difference](https://www.quora.com/Regression-statistics-What-is-the-difference-between-Ordinary-least-square-and-generalized-least-squares)) 3.Penalized Least Squares (Lasso and Ridge)

**2. Describe the formula for logistic regression and how the algorithm is used for binary classification.**
* <img src="Q2_Formula.png" width="200" height="50" /> We can use the result of f(x) as the probability of a data point being labeled as positive case. There is a cutoff value to choose to label the data points. For detailed mathematical derivation, please refer the [post](http://www.win-vector.com/blog/2011/09/the-simpler-derivation-of-logistic-regression/)
