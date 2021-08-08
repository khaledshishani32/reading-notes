# How To Run Linear Regressions In Python Scikit-Learn
---

### Scikit-learn is a Python package that simplifies the implementation of a wide range of Machine Learning (ML) methods for predictive data analysis, including linear regression.

##### Linear regression can be thought of as finding the straight line that best fits a set of scattered data points: 

![](https://cdn.activestate.com/wp-content/uploads/2021/03/Model-linear-regressions.png)

---
## key concepts of scikit-learn’s linear regression method:
- Best Fit – the straight line in a plot that minimizes the deviation between related scattered data points.
- Coefficient – also known as a parameter, is the factor a variable is multiplied by. In linear regression, a coefficient represents changes in a Response Variable .
- Coefficient of Determination – the correlation coefficient denoted as 𝑅². Used to describe the precision or degree of fit in a regression. 
- Correlation – the relationship between two variables in terms of quantifiable strength and degree, often referred to as the ‘degree of correlation’.  Values range between -1.0 and 1.0. 
- Dependent Feature – a variable denoted as y in the slope equation y=ax+b. Also known as an Output, or a Response. 
- Estimated Regression Line – the straight line that best fits a set of scattered data points.
- Independent Feature – a variable denoted as x in the slope equation y=ax+b. Also known as an Input, or a predictor. 
- Intercept – the location where the Slope intercepts the Y-axis denoted b in the slope equation y=ax+b. 
- Least Squares – a method of estimating a Best Fit to data, by minimizing the sum of the squares of the differences between observed and estimated values.
- Mean – an average of a set of numbers, but in linear regression, Mean is modeled by a linear function.
- Ordinary Least Squares Regression (OLS) – more commonly known as Linear Regression. 
Residual – vertical distance between a data point and the line of regression .
- Regression – estimate of predictive change in a variable in relation to changes in other variables .
- Regression Model – the ideal formula for approximating a regression.
- Response Variables – includes both the Predicted Response (the value predicted by the regression) and the Actual Response, which is the actual value of the data point .
- Slope – the steepness of a line of regression. Slope and Intercept can be used to define the linear relationship between two variables: y=ax+b.
- Simple Linear Regression – a linear regression that has a single independent variable.

![](https://cdn.activestate.com/wp-content/uploads/2021/03/Model-linear-regressions-figure.png)

# Example : Create a Linear Regression and Display it 

#### # Import the packages and classes needed for this example:
#### import numpy as np
#### import matplotlib.pyplot as plt
#### from sklearn.linear_model import LinearRegression

#### # Create random data with numpy, and plot it with matplotlib:
#### rnstate = np.random.RandomState(1)
#### x = 10 * rnstate.rand(50)
#### y = 2 * x - 5 + rnstate.randn(50)
#### plt.scatter(x, y);
#### plt.show()

#### # Create a linear regression model based the positioning of the data and Intercept, and predict a Best Fit:
#### model = LinearRegression(fit_intercept=True)
#### model.fit(x[:, np.newaxis], y)
#### xfit = np.linspace(0, 10, 1000)
#### yfit = model.predict(xfit[:, np.newaxis])

#### # Plot the estimated linear regression line with matplotlib:
#### plt.scatter(x, y)
#### plt.plot(xfit, yfit);
#### plt.show()



---
### references :
---
[towardsdatascience](https://towardsdatascience.com/)