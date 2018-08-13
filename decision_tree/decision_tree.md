# Decision Tree (CART)
#### Hello, Decision Tree
A decision tree, also referred to as Classification and Regression Tree (CART), is a powerful algorithm that can beautifully illustrate how an algorithm learns from data. A decision tree is essentially a binary tree which finds optimal splits in features in order to classify or predict continuous values. So what exactly is meant by finding optimal splits?

Below are links to see a decision tree in action

* [from scratch](https://github.com/jimmychimmyy/machine_learning_notes/blob/master/decision_tree/decision_tree.ipynb)
* [using sklearn]()

#### How does it work?

A decision tree contains 2 main elements: nodes and edges.

Each node on a decision tree represents (you can also think of it as containing) a single feature and a split point for that feature. The split point splits the values of its feature into two separate classes. Each node has either 0 or 2 children. Children nodes are connected to their parent node by an edge. On a decision tree, you start with a root node with a single feature and a split point, then proceed to add edges and children as needed (*this is how a decision tree learns*). When a decision tree is complete, any node that has 0 children is a decision leaf (a leaf node) that tells you a prediction.

Our job, when creating a decision tree, is to figure out what features to use in what order to construct a tree that provides predictions with the least amount of error.

#### Algorithm:

1. Calculate [entropy](#entropy)/gini-coefficient of every feature in set S
2. Split set S into subsets using feature with minimum entropy/gini-coefficient
3. Add node to decision tree with this feature
4. Repeat above steps for all remaining features

##### Parameters:
* X - vector where each element is an instance
* Y - vector where each element is an instance

##### Hyperparameters:


#### Cost Function

We will be using the **Gini Index** as the cost function for decision trees. A Gini score tells you how well a point in your data splits your total data into two classes. A Gini score of 0 is a perfect split: imagine you have two normal distributions sitting side by side with no overlap. A Gini score of 0.5 is the worst possible split: imagine you have the same two normal distributions but they overlap, almost seemingly they make a single multimodal distribution.

###### add image for clarification

#### What is Greedy Splitting?

#### <a name="entropy"></a>What is Entropy?

#### What is a Stopping Criterion?

#### What is Pruning?

#### How to evaluate performance of Decision Tree

#### Assumptions of Decision Tree

#### Things to watch out for

#### Tips and Tricks

#### Sources
1. https://machinelearningmastery.com/classification-and-regression-trees-for-machine-learning/
2. https://en.wikipedia.org/wiki/ID3_algorithm
3. https://datascience.stackexchange.com/questions/10228/gini-impurity-vs-entropy
