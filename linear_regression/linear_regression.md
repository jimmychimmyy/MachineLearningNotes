# Linear Regression

#### Hello, Linear Regression

The classic example of Linear Regression is to predict housing prices given some labeled data.

#### How does it work?

##### Think `y = (w0) + (w1)(x)`

1. `y = output (dependent variable)`
2. `x = input (independent variable)`
3. `w0 = coefficent`
4. `w1 = coefficent`

Let m = the number of instances (number of rows)

Let n = number of features (number of columns)

x and y are given by our training data

*To learn our data, we need to find the values of w0 and w1.*

Once we know the values of w0 and w1, we can use this equation to predict y for a new x.

To summarize, our model learns our coefficents and is then able to make new predictions.

#### Cost Function

##### Note that:
Remember that by definition, simple linear regression has a single independent variable and a single dependent variable

As your data becomes more complex you will have more independent variables (features) and you will need to use [Multilinear Regression](https://github.com/jimmychimmyy).

#### Assumptions of Linear Regression

Linear Regression makes five key assumptions about your data:
1. Linear relationship
2. Multivariate normality (are your variables distributed normally?)
3. Little to no multicollinearity (multicollinearity occurs when the independent variables are too highly correlated with each other)
4. No Auto-Correlation
5. Homoscedasticity

#### Example using sklearn

#### My Implementation

#### What kind of problems can it solve?

#### Things to watch out for

#### Sources
1. https://www.youtube.com/watch?v=ZkjP5RJLQF4 <- this is an amazing source to really grasp the concept of linear regression
2. http://www.statisticssolutions.com/assumptions-of-linear-regression/
