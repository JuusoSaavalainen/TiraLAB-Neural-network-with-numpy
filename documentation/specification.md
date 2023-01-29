
# Specification document

This project will aim to implement a simple neural network with [MNIST](http://yann.lecun.com/exdb/mnist/) database. The project will possibly have GUI if the time is right and at least command line UI. The trained model will classify the handwritten digits from 0-9 and the model will be able to handle similarly formed data. The implementation will not use any third-party libraries like Tensorflow or Pytorch. Matrix operations will be handled with the NumPy library and the project will be fully written with Python 3.
> NOTE: This approach was chosen because classification with mnist is a really simple problem in the space of machine learning problems. Sometimes even called the "Hello World" of ML. Also, my way of doing it makes me dig into algorithms, logic, and the math behind the chosen approach. Those same things underlying many today widely used libraries
# Algorithms and time complexity
## Model
The main thing in my approach to the classification problem is this so-called neural network and optimizing the weights of every single connection accordingly. That will be done via a few algorithms that will do the tuning during the training. The first thing we use is forward propagation/forward pass which will be used to feed the data from input layers to output and with that calculate the activation of each output node. Some activation functions will also be used during the training to squish the values of a node to intervals 0-1. After the forward pass, we will be wanting to tune the weights accordingly so we can minimize the loss function. The loss function is defined as the price of the inaccuracy of the wanted result and the given result by the model. Inputs of the model will be 28x28-sized vectors/arrays. And it will probably have a simple structure consisting total of 4 layers and its so-called [FNN](https://en.wikipedia.org/wiki/Feedforward_neural_network) / [MLP](https://en.wikipedia.org/wiki/Multilayer_perceptron).
## Backpropagation
So the biggest focus in the implementation is the backpropagation algorithm which combined with [gradient descent](https://en.wikipedia.org/wiki/Gradient_descent) algorithm will be able to calculate the updated weights in each learning loop. Numpy arrays will be the main data structure. What it comes to time complexity it will be heavily dependent on the structure of the neural network and the size of it each layer. That is something that will be changing during the process of finding the right balance with the model. But generally speaking, the backpropagation algorithm will be most likely used in the so-called stochastic form so the time complexity will also depend on the batch size chosen to train the model. In the model with 4 total layers the big 0 notation of a single training cycle is O(t * (ij + jk + kl)) where t denotes the batch size of one epoch, i j k and l denotes the nodes in the layers. Space complexity should be O(2m +1) where m denotes each component. These will be evaluated again after the structure of the network is set up.    

# Course details

I am capable to write python and i wish to peer review projects made with it. I study in the computer science bachelor's program and i will be doing documentation using the markdown language during this course in English. ENG will be the chosen language for anything related to this project.

## Sources / links
[DeepAi](https://deepai.org/machine-learning-glossary-and-terms/feed-forward-neural-network)

[3blue1brown](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi) very good video series to understand the fundamentals of this topic and the maths laying behind the whole process

[Backpropagation](https://en.wikipedia.org/wiki/Backpropagation) 

[Paper](https://arxiv.org/abs/1810.03218) including analysis of the time cmplx of NN

[Deep Learning](https://www.deeplearningbook.org/) An MIT Press book