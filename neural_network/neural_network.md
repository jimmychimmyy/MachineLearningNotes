# Artificial Neural Network
#### Hello, Artificial Neural Network
Artifical neural networks (ANN) are machine learning models inspired by biological neural networks but aside from inspiration have little relation.

Below are links to see a neural network in action

* [from scratch](https://github.com/jimmychimmyy/machine_learning_notes/blob/master/neural_network/neural_network.ipynb)
* [using keras](https://github.com/jimmychimmyy/machine_learning_notes/blob/master/neural_network/keras_neural_network.ipynb)

#### How does it work?

In this section I will be discussing the most common model of an ANN: the 3 layer fully connected backpropogation model.

From a a top-down perspective, this ANN has 3 layers: the input layer, the output layer, and the hidden layer. All ANNs follow this structure however they may have more than a single hidden layer. In each layer, there is some number of nodes which are all connected by edges to every single node in the previous and subsequent layer.

![ANN](http://cs231n.github.io/assets/nn1/neural_net.jpeg "ANN")

Each node has value of [0.0, 1.0] where 0 represents "off" and 1 represents "on".

Each weight has some value ...

###### How do we select the number of nodes in each layer?
The number of nodes in the input layer is determined by the number of features in your feature vector.

The number of nodes in your output layer is determined by the problem (classification vs regression vs etc.). For example, in regression, there will be a single output node indicating some continuous value. In classification there will be the same number of output nodes as there are classes. Note that, for the special case of  binary classification an ANN may have a single node in its output layer where the value of the node is either true of false for belonging in the class.

The number of nodes in your hidden layer is often debated. However, a good starting point would be to have a number equal to the mean of the input and output layer.

Some ANNs add one extra node in each layer for bias.

###### How do we determine the number of hidden layers?

There are numerous ANN architectures but a good rule starting point would be to have a single hidden layer. *A single hidden layer is sufficient for most problems*.

#### Algorithm
1. Initialize ANN
2. Randomly assign edges values so that they are non-zero
3. Compute product of each node and each of its weight
4. In the next layer, for each node, take the sum of the product where each edge connects previous layer nodes to this node.
5. Apply some activation function to the resulting sum, this becomes the new value for this node.
6. Repeat steps 3 - 5 until all nodes in output layer have been updated.
7. [Backpropagate]()

*Note that steps 1 - 6 are referred to as feedforward*

![TrainingANN](https://cdn-images-1.medium.com/max/1280/1*vLRcDyU-NVyrWJLtYrAhew.jpeg "TrainingANN")

###### *Note that the algorithm I have described here is a cost heavy description of how to build an ANN. In practice, if you are implementing your own ANN you should use the dot product to calculate the sum of the products of nodes and weights. You may look to my [implementation](https://github.com/jimmychimmyy/machine_learning_notes/blob/master/neural_network/neural_network.ipynb) for more details.*

###### Parameters:
* weights

###### Hyperparameters:
* Number of Hidden Layers
* Number of Nodes in Hidden Layers
* Activation Function
* Learning Rate
* Momentum
* Epochs
* Batch Size

###### Cost Function:

You may use a number of cost functions for ANNs, for the purpose of these notes, I will be using the commonly used Mean Squared Error (MSE).

###### Discussion on which cost function to use

#### What is Pruning?


#### Sources
1. https://stats.stackexchange.com/questions/181/how-to-choose-the-number-of-hidden-layers-and-nodes-in-a-feedforward-neural-netw
2. http://cs231n.github.io/assets/nn1/neural_net.jpeg
3. https://towardsdatascience.com/how-to-build-your-own-neural-network-from-scratch-in-python-68998a08e4f6
4. https://www.analyticsvidhya.com/blog/2014/10/ann-work-simplified/
5. https://medium.com/deep-math-machine-learning-ai/chapter-7-artificial-neural-networks-with-math-bb711169481b
6. https://cdn-images-1.medium.com/max/1280/1*vLRcDyU-NVyrWJLtYrAhew.jpeg
7. https://towardsdatascience.com/what-are-hyperparameters-and-how-to-tune-the-hyperparameters-in-a-deep-neural-network-d0604917584a
