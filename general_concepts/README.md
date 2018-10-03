# General Concepts

In this section I will be explaining some of the general concepts that apply to machine learning.

#### Table of Contents
1. [Bias Variance Tradeoff](#biasvariance)
2. [Cross Validation](#crossval)
3. [Maximum Likelihood Estimation (MLE)](#mle)

## <a name='biasvariance'></a> Bias Variance Tradeoff
The bias-variance tradeoff in machine learning is a property of machine learning where models with high bias have low variance, and models with low bias have high variance.

#### What is Bias?

Bias is error that is a result of assumptions made by the machine learning algorithm.

High bias will cause the algorithm to [underfit]() the data.

High bias algorithms are usually less complex
* Linear Algorithms
* Parametric Algorithms

#### What is Variance?

Variance is error from noise in the training data.

High variance will cause the algorithm to [overfit]() the data.

High variance algorithms are usually more complex
* Non-linear Algorithms
* Non-parametric Algorithms

#### Why do we want to minimize both bias and variance?

`Total Error = bias^2 + variance + irreducible error`

The goal of machine learning is to create models with the least possible amount of error that also generalize well to unseen data. Minimizing bias means reducing the difference between our model's predictions and the actual output. Minimizing variance means reducing our model's sensitivity to noise and preventing it from "memorizing" the training data.

High bias makes for poor predictions because it cannot model complex data.

High variance makes for bad generalizations because it memorizes training data and consequently random noise instead of desired patterns in the data.

#### How do we actually achieve low bias and variance?

There is no possible way to have both low bias and low variance. Instead, we need to find a balance of bias and variance that minimizes total error.

#### How do I know if my model underfits or overfits?

* Dataset Split
* [Cross Validation]()
* Bootstrap

#### Sources
1. https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff
2. https://elitedatascience.com/bias-variance-tradeoff
3. https://stats.stackexchange.com/questions/256141/mathematical-intuition-of-bias-variance-equation
4. https://stats.stackexchange.com/questions/81576/how-to-judge-if-a-supervised-machine-learning-model-is-overfitting-or-not
5. https://www.quora.com/How-do-we-detect-overfitting-and-under-fitting-in-Machine-Learning

## <a name='crossval'></a> Cross Validation
How well will my model perform on unseen data? (How well does my model generalize?)

If a model sees the entire dataset during training it will undoubtedly perform exceedingly well on the same dataset. This is why before learning a model, it is important to partition our dataset into training and testing data. Cross-validation takes this idea one step further.

Cross-Validation tells us how well the model will generalize on unseen data. The high level idea of cross-validation is to partition part of the training set into a validation set. The training set allows us to see how well our model has fitted our parameters. We then make predictions on the validation set which allows us to fine tune the hyperparameters.

###### Remember:
1. The model's parameters are fitted using the training set.
2. We evaluate the fitted model's predictions using the validation set (we tune hyperparameters here accordingly).
3. We evaluate the final fitted model's predictions using the test set.

#### Types of Cross-Validation
* Holdout Method
* K-Fold Cross Validation
* Stratified K-Fold Cross Validation
* Leave-P-Out Cross Validation

#### Holdout Method

Partition data into 3 subsets: training, validation (holdout), testing.

Train your model using the training set. Use the validation set to see how well the model performs on unseen data. Use testing set for final estimate of the model's performance.

Typically, you will split your training and testing data into 80% and 20% respectively. To obtain your holdout set, you split your training set further.

###### Pros:
* runs once

###### Cons:
* higher variance since training data size is reduced

#### K-Fold Cross Validation

The high-level idea of k-fold cross-validation is to partition the training data into **k** folds (subsets). We then train our model using **(k - 1)** folds of the data while saving the **kth** fold as a validation set to evaluate our model's performance. We repeat this process **k** times, using each fold of the training data as the validation set once. The error we get from the evaluation of the **kth** fold is an approximation of our model's generalization error. We sum and divide the error by **k** in order to get the average error.

###### Pros:
* has lower variance than holdout method
* good to use if you have limited data

###### Cons:
* model is trained k separate times

#### Stratified K-Fold Cross Validation

Similar to k-fold cross validation, the difference is that in stratified k-fold the folds are partitioned carefully to ensure that each fold contains an approximately equal number of class labels (target class). In other words, we want to keep the proportion of classes constant across all folds.

Basically, you can think of this as k-fold cross validation for classification problems.

#### Leave-One-Out Cross Validation

In leave-one-out (LOO-XVE), we use all the training data, save one instance, to train the model. Like k-folds, we repeat this process **M** times, where **M = total number of instances**. We sum the error and get an average.

###### When should I use Cross-Validation?

###### What is the ideal ratio of Training:Validation:Testing?

#### Sources
1. https://towardsdatascience.com/cross-validation-in-machine-learning-72924a69872f
2. https://www.quora.com/What-is-cross-validation-in-machine-learning
3. https://www.kdnuggets.com/2017/08/dataiku-predictive-model-holdout-cross-validation.html
4. https://www.datarobot.com/wiki/training-validation-holdout/
5. https://cimentadaj.github.io/blog/2017-09-06-holdout-and-crossvalidation/holdout-and-crossvalidation/
6. https://machinelearningmastery.com/k-fold-cross-validation/

## <a name='mle'></a> Maximum Likelihood Estimation (MLE)
