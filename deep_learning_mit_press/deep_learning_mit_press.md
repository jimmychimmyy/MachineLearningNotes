# Deep Learning. MIT Press (Goodfellow, I., Benigo, Y., and Courville, A.)

### Questions
* How do the hidden layers of deep nns extract increasingly abstract features?
    * is it that they see enough training samples and the same pattern is found in the same hidden layer for many instances?
* can deep learning be applied to NLP, vision, motion planning, and speech recognition?
* what are neural Turing machines?

### Introduction
* there are 2 main ways of measuring depth of a model
  1. number of sequential instructions that must be executed
  2. depth of the graph describing how concepts are related to each other
* most nns today are based on model neuron called **rectified linear unit**
* as of 2016, a rough rule of thumb: supervised deep learning algorithm will generally achieve acceptable performance with around 5000 labeled examples per category and will match or exceed human performance when trained on dataset containing at least 10 million labeled examples

*"We contend that machine learning is the only viable approach to building AI systems that can operate in complicated real-world environments"* (Page 8)

## Part 2 Modern Practical Deep Networks
### Deep Feedforward Networks
* deep feedforward networks == feedfoward neural networks == multilayer perceptrons
* feedforward defines mapping `y = f(x, theta)` and learns the value of theta that results in the best function approximation
* feedforward means no feedback, nns with feedback are called recurrent nns
* A classifier `y = f*(x)` maps x to y
* a feedforward network defines mapping `y = f(x; theta)` and learns theta that results in the best approximation of `f*(x)`


**nns are called networks because they are typically represented by composing together many different functions**

How a feedforward nn model works:
* Given 3 functions connected in a chain: f1, f2, f3
we get: `f(x) = f3(f2(f1(x)))`
  * f1 is called the first layer, f2 is the second layer, and so on. The total length of this chain gives the **depth** of the model
* final layer is **output layer**
* the learning algorithm decides how to produce desired best approximation output but the training data does not show the desired output of each **hidden layer**

**Starting with Linear Models:**

*To extend linear models to represent nonlinear functions of x we can apply the linear model to a transformed input of g(x) where g is a nonlinear transformation*. We can also apply the kernel trick to obtain a nonlinear ml algorithm based on implicitly applying the transformation mapping. Think of g as providing a set of features providing a new representation for x. So how to choose the mapping for x?

**In modern nns the default recommended activation function is the rectified linear unit (ReLU)**

TODO: Re-read 6.1 Example XOR

#### Cost Function
*"The principle of maximum likelihood provides a guide for how to design a good cost function for nearly any kind of output layer"*
If we define a conditional distribution: p(y|x; theta), the principle of maximum likelihood suggests that we use -log p(y|x; theta) as our cost function.

#### Architecture
*"The ideal network architecture for a task must be found via experimentation guided by monitoring the validation set error"*

#### Universal Approximation Properties and Depth
* feedforward nns with hidden layers provide universal approximation framework
* **universal approximation theorem** ...
* in summary, a feedforward nn with a single layer is sufficient to represent any function but the layer may be infeasibly large and may fail to learn and generalize correctly; deeper models can reduce the number of units required to represent the desired function and can reduce the amount of generalization error
