# Logistic Regression

#### Hello, Logistic Regression
Contrary to its name, logistic regression is actually a classification algorithm. Logistic regression transforms its input using the sigmoid function (a.k.a the logistic function) to produce probability values as output. These resulting probability values are used to sort instances into discrete classes based on some user-supplied threshold.

Below are links to see Logistic Regression in action
* [from scratch](https://github.com/jimmychimmyy/machine_learning_notes/blob/master/logistic_regression/logistic_regression.ipynb)
* [using sklearn]()

#### How does it work?

```
Let x_i be an input feature vector with length n
Let m = number of input feature vectors
Let a_i be a vector that is same length as x_i

p(y_i|x_i) = 1 / 1 + e^z where z = a_i * x_i + b
can also be written as: e^z / (1 + e^z)
```

#### Loss function

```
L(a_i, b|X, y) = - log p(Y|X, a_i, b)
= log ∏[p(y_i|x_i, a_i, b)]


∂L/∂a_ij = sum_i:1_n[y - p(y_i=1|x_i, b, a_i) * x_ij]
```

### Multinomial Logistic Regression

```
p(y_i = c_j|x_i) = e^z / sum_l:1_k[e^y]
where z = x_i * a_j + b_j
where y  = x_i * a_l + b_l

each class c_j has its own classification parameters a_j and b_j
there are k total classes
```

#### Algorithm:

###### Parameters:

###### Hyperparameters:

#### What is an Activation Function?

An activation function checks if our output is above a certain decision threshold, if so, our model will classify the instance as true.

For example, if we set our decision threshold to be 0.5, then any instance with 0.5 or greater probability will be classified as true and any less than 0.5 as false.

#### Cost Function

#### How to evaluate performance of Logistic Regression

#### Assumptions of Logistic Regression

#### Things to watch out for

#### Tips and Tricks

#### Sources
1. https://machinelearningmastery.com/logistic-regression-for-machine-learning/
2. http://ml-cheatsheet.readthedocs.io/en/latest/logistic_regression.html
3. https://medium.com/the-theory-of-everything/understanding-activation-functions-in-neural-networks-9491262884e0
4. https://stats.stackexchange.com/questions/278771/how-is-the-cost-function-from-logistic-regression-derivated
