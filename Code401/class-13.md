# Reading Assignment 13

## Linear Regressions

---

### How to Run Linear Regression in Python

---

- To start off with making a linear regression model, you import it from `sklearn.linear_model` then you store the `LinearRegression` object as a variable for ease of use and one helpful thing to do is to type the object and press tab to see all the available functions on the object.
- Some of the most important functions are;
  - `lm.fit()` which fits a linear model
  - `lm.predict()` which predicts using the linear model with estimated coefficients
  - `lm.score()` which returns the coefficient of determination which is a measue of how well observed the outcomes are replicated by the model.
- You won't often implement linear regression on an entire data set, you will split the data sets into a training set and a test set so you can train the model on training data and then see how it performs on test data.
- To do this, the best way is to use `train-test split` which divides the data randomly into the two sets so as to ensure the training and test sets are comparable in variences for the data.
- A good way to visualize errors in the data is to use a residual plot. If the data is scattered around line zero then you did your job well.

### Introduction to Simple Linear Regressions

---

- Regression Analysis is the exploration of the relationship between a response variable and one or more explanatory variables.
- If there is only one explanatory variable, it is Simple Linear Regression and if there is more than one, it is Multiple Regression.
- In Simple Linear Regression, the two variables are typically represented by the variables of `x` and `y` and each dataset is a set of `x`,`y` pairs.
- Typically, when deciding if a dataset is consistent enough to build a prediction of of, the question is;
  - Is there enough strong evidence of a relationship between the explanatory variable and the response variable.
- A linear relationship is represented by;
  - > <math xmlns="http://www.w3.org/1998/Math/MathML"><msub><mi>&#x3bc;</mi><mrow><mi>Y</mi><mo>&#xA0;</mo></mrow></msub><mo>|</mo><mo>&#xA0;</mo><mi>X</mi><mo>&#xA0;</mo><mo>=</mo><mo>&#xA0;</mo><msub><mi>&#x3b2;</mi><mn>0</mn></msub><mo>&#xA0;</mo><mo>+</mo><mo>&#xA0;</mo><msub><mi>&#x3b2;</mi><mn>1</mn></msub><mo>&#xA0;</mo><mi>X</mi></math>
  - In this equation, <math xmlns="http://www.w3.org/1998/Math/MathML"><msub><mi>&#x3b2;</mi><mn>0</mn></msub></math> is equal to the Y intercept and <math xmlns="http://www.w3.org/1998/Math/MathML"><msub><mi>&#x3b2;</mi><mn>1</mn></msub></math> is equal to the Slope.
- This line plots a line which represents the relationship between y and x and says that if you know the value of x, then you can know the value of y, but this is rarely correct as the true data will vary along the line and the line represents the mean value of y.
- To account for the variablity of the data, you add to the line plot equation with <math xmlns="http://www.w3.org/1998/Math/MathML"><mo>+</mo><mo>&#xA0;</mo><mi>&#x3f5;</mi></math> to the end to represent the random error component.
- Because of this, you use sample data to get the estimated regression line. The equation for this looks like this;
  - > <math xmlns="http://www.w3.org/1998/Math/MathML"><mi>Y</mi><mo>&#xA0;</mo><mo>=</mo><mo>&#xA0;</mo><msub><mi>&#x3b2;</mi><mn>0</mn></msub><mo>&#xA0;</mo><mo>+</mo><mo>&#xA0;</mo><msub><mi>&#x3b2;</mi><mn>1</mn></msub><mo>&#xA0;</mo><mi>X</mi></math>
  - Except it has the `^` symbol above the Y, and both <math xmlns="http://www.w3.org/1998/Math/MathML"><mi>&#x3b2;</mi></math>'s.
- To get the values for both Betas, you use the method of least squares.
