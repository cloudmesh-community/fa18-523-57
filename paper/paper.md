# PyTorch :hand: :exclamation: fa18-523-57

| Divya Rajendran
| divrajen@iu.edu
| Indiana University
| hid: fa18-523-57
| github: [:cloud:](https://github.com/cloudmesh-community/fa18-523-57/tree/master/paper)

* do not remove the :exclamation: this is for the instructors a sign that we
	reviewed

---

Keywords: Hid fa18-523-57, Deep Learning, gradient descents, Autograd, Neural Networks, Tensors, Python

---

PyTorch [@paszke2017automatic] is a python based deep learning framework used
for scientific calculations. It is popular among Neural Nets and Deep Learning
developers due to its faster implementation of the algorithms and the maximum
flexibility of its use. It is also used as a replacement for NumPy
[@fa18-523-57-NumPy], an existing package, available in Python on scientific
computing. The reason being, PyTorch mimicked most of NumPy's functionality with
an addition of increased speed by making use of the Graphical Processing Unit
(GPU) [@fa18-523-57-PyTorch].

Being written in a commonly used language by Machine Learning and Artificial
Intelligence developers, Python, PyTorch has been gaining popularity since its
inception in 2016 [@fa18-523-57-PyTorch-Wikipedia]. It is also less complex and
easy to use when compared to existing Deep Learning frameworks like TensorFlow
[@fa18-523-57-TensorFlow], Keras [@fa18-523-57-Keras], Caffe
[@fa18-523-57-Caffe], Chainer [@fa18-523-57-Chainer],MXNet [@fa18-523-57-MXNet],
CNTK [@fa18-523-57-CNTK], Deeplearning4j [@fa18-523-57-DL4J].

PyTorch has been developed by the Artificial Intelligence group at Facebook
[@fa18-523-57-PyTorch-Wikipedia] and is a successor framework of Torch
[@fa18-523-57-Torch] and has been built on it. Torch is a computing framework
for scientific calculations wrapped in Lua, a programming language written in a
general purpose programming language C [@fa18-523-57-C]. This framework, Torch
runs even in constrained platforms through LuaJIT [@fa18-523-57-LuaJIT] a
platform specific compiler. It is used extensively to implement machine learning
and deep learning algorithms [@fa18-523-57-PyTorch-Wikipedia]. It has a
plethora of packages commonly used for Machine Learning, Signal Processing,
Computer Vision among others, these have been inherited into PyTorch
as well [@fa18-523-57-Torch].

PyTorch seamlessly integrates all the packages which Torch offers and builds all
of its functionality using Python, making Python its integral part. This makes
the implementation of algorithms even faster than Torch. The main package of
Torch and PyTorch is *torch* using which we can train neural networks, define
the loss function and calculate the gradients for loss function
[@fa18-523-57-PyTorch-Wikipedia].


## Background

Before we start using PyTorch, we need to have a background or working knowledge
on the below concepts.

Keywords: #Deep Learning, Neural Networks, Tensors, Computational Graph, Autograd
					, Auto Differentiation, Backpropagation

### Deep Learning

Deep Learning [@fa18-523-57-Deep-Learning-wiki] is a branch of Machine Learning
which takes its inspiration from the function and structure of a human brain
[@fa18-523-57-Deep-Learning]. It has a sub architecture called neural network
which has been vastly used in different fields of computer vision, audio and
video signal processing, natural language and speech recognition and such
[@fa18-523-57-Deep-Learning-wiki].

### Neural Networks {#Neural Networks}

Neural Nets [@fa18-523-57-Neural-Nets] is a collection of various connected
nodes called neurons mimicking the neuron structure in the human brain. Each
neuron receives an input, processes this input by performing a set of operations
and then sends it to a next layer in the neural nets. Each layer has a weight
and bias associated to it, on which a computation is done. This processing is
based on some pre-defined function, a gradient descent algorithm, which
transforms the input in each layer and this entire process is repeated a huge
number of times till the error calculated is diminished
[@fa18-523-57-Neural-Nets].

### Tensors {#Tensors}

Tensor [@fa18-523-57-Tensor] is an inbuilt data structure in PyTorch and can be
defined as a matrix of matrices or can be defined as a multi-dimensional array
with dimensions greater than 3. So a tensor with 3 dimensions is called a 3-D
tensor and a tensor with 4 dimensions is called a 4-D tensor
[@fa18-523-57-Tensor]. This tensor are used on a GPU which accelerates the
computing process and calculation time on matrix operations when compared to
existing NumPy's ndarrays [@fa18-523-57-PyTorch].

### Computation Graph {#Computational Graph}

A computational graph [@fa18-523-57-graph] is a internal representation of the
operations performed during the neural nets training. It is also called a data
graph and is also an inbuilt data structure in PyTorch. It consists of a set of
nodes and edges, with nodes representing each operation and edges representing
the values being sent from each operation from one layer to another layer in
neural networks [@fa18-523-57-graph].

### Auto Differentiation {#Auto Differentiation}

Auto Differentiation [@fa18-523-57-Differentiation] is a series of techniques
used to numerically calculate the derivative of the transformation and loss
functions defined in our neural networks [@fa18-523-57-Differentiation].z

### Backpropagation {#Backpropagation}

Back propagation [@fa18-523-57-Backpropagation] is a technique in neural
networks which calculates the gradient values for the peaks and troughs of the
loss function and send the error values obtained to the previous layer going in
the reverse or backward direction [@fa18-523-57-Backpropagation].

### Autograd {#Autograd}

Autograd [@fa18-523-57-Autograd] is a function in the *torch* library of PyTorch
which calculates the gradients of the transformation and loss functions used in
neural networks. This function uses a technique called tape-based
Auto-Differentiation [@fa18-523-57-PyTorch-Started], a kind of the
Auto-Differentiation. This technique saves the operations performed in each
layer of the neural network in a reverse order, mimicking how a tape recorder
works. This function also saves the gradients calculated in each layer of neural
nets and replays them in a reverse order. This implementation in PyTorch is
faster than the same implementation in existing frameworks like TensorFlow
[@fa18-523-57-PyTorch-Started]. We also use this function to train weights for
neural networks through back propagation

## Getting Started

If you have never used PyTorch before you need to install PyTorch, check
[@fa18-523-57-PyTorch-requirements] for more instructions on the system
requirements and different ways to install PyTorch
[@fa18-523-57-PyTorch-installation].

In your system terminal or command prompt, enter the below line to install the
PyTorch library.

```python
pip install torch torchvision
```

You would see a message similar to the below in your command or terminal window.

```bash
$ pip install torch torchvision
```

To use PyTorch we need to first import the library *torch*. A sample
initialization of tensors using PyTorch is done as below.

```python
from __future__ import print_function
import torch
```

#### Creating an empty matrix

```
torch.empty(4, 3)
```


#### Creating a randomly initialized matrix

```
torch.rand(4, 3)
```


#### Constructing a tensor

```
torch.tensor(torch.rand(4, 3))
```

Step by step instructions for using PyTorch can be found at
[@fa18-523-57-instructions].

## Implementation

PyTorch can be initialized using the package *torch*. It contains the below
functions.

1. *torch.nn* is a library of functions used to train or build the neural
	 networks [@fa18-523-57-PyTorch-modules].

2. *torch.nn.Linear* is a function which applies a transformation linear in
	 nature on the incoming values [@fa18-523-57-PyTorch-modules].

3. *torch.nn.Sequential* is a function used to initialize a model with a linear
	 stack of layers [@fa18-523-57-PyTorch-modules].

4. *torch.nn.MSELoss()* is used to initialize the loss function and also
	 calculates the error between the input and the output layer in the neural
	 nets [@fa18-523-57-PyTorch-modules].

5. *torch.optim* is a function which defines an optimizer algorithm which
	 updates the weights at each layer [@fa18-523-57-PyTorch-modules].

Let us see an example of how to use these above functions to train a neural
network as below.

##### Define the neural network
```python
###########################################################################
#    Title: Classifying Text with Neural Networks and Pytorch
#    Author: Mesquita, Déborah
#    Date: Oct 25, 2017
#    Code version: 1
#    Availability: https://github.com/dmesquita/understanding_pytorch_nn
#
###########################################################################
import torch
import torch.nn as nn

class OurNet(nn.Module):
 def __init__(self, input_size, hidden_size, num_classes):
     super(Net, self).__init__()
     self.layer_1 = nn.Linear(n_inputs,hidden_size, bias=True)
     self.relu = nn.ReLU()
     self.layer_2 = nn.Linear(hidden_size, hidden_size, bias=True)
     self.output_layer = nn.Linear(hidden_size, num_classes, bias=True)

 def forward(self, x):
     out = self.layer_1(x)
     out = self.relu(out)
     out = self.layer_2(out)
     out = self.relu(out)
     out = self.output_layer(out)
     return out
```
The above code initiates the neural network with two hidden layers and one
output layer. The function *nn.Linear* transforms the input layer data
linearly, by multiplying the data with weights and adding a bias value. The
transformation of our neural network is taken through the function *forward*
which we defined above. In this function we call the initialized values and
functions and transform the output and return this value.
[@fa18-523-57-PyTorch-Code]

To update the weights for our neural network, we use the optimizer algorithm
*Adaptive Moment Estimation (Adam)* through the package *torch.optim*. This
optimizer holds the state of the object and the components based on the gradient
computation. To calculate the loss we use a function called
*torch.nn.CrossEntropyLoss*. Below is a sample code on constructing the
optimizer [@fa18-523-57-PyTorch-Code].

##### Constructing optimizer
```python
net = OurNet(input_size, hidden_size, num_classes)
optimizer = torch.optim.Adam(net.parameters(), lr=learning_rate)
criterion = nn.CrossEntropyLoss()
```
The step *OurNet()* is our initization step for the neural nets we created. We
get the initialized neural nets parameters and use it to initialize our
optimizer function. Our next step would be to load a dataset from sklearn
datasets, or any other set of datasets and use it to test our functions written.
The entire code for initializing neural networks, loss and optimizer functions,
including training and testing our models while applying them to a dataset of
our choice is available can be found at [@fa18-523-57-Code].

## Advantages of PyTorch Over Existing Frameworks

When we compare PyTorch over the existing frameworks like TensorFlow, Caffe,
Keras, Chainer and such, the below are the most promising advantages.

1. Ramp Up Time is the time taken to execute all the threads or layers and their
	 iterations. This time for code execution using PyTorch is much faster than
	 its competitor TensorFlow, in that it uses dynamic creation of graphs
	 rather than the static ones in TensorFlow. Here, the compilation time for the
	 code is much smaller for PyTorch, it uses GPU to increase the speed of
	 execution and the graph is built during run time, making it significantly
	 faster than TensorFlow [@fa18-523-57-PyTorch-tensorflow].

2. Debugging in PyTorch is easy as the underlying language is Python, which is
 	 a common language used by developers and its quite easier when compared to
	 TensorFlow. We can use print statements to keep track of what values our
	 variables take and to identify where our code fails
	 [@fa18-523-57-PyTorch-tensorflow].

3. Data Loading is much faster in PyTorch as the APIs for loading the data are
   designed in a manner to best utilize its parallelizing data loading
	 capability. One can use either NumPy, Pandas or any other library of choosing
	 and can load data quite faster as PyTorch utilizes GPU
	 [@fa18-523-57-PyTorch-tensorflow].

4. PyTorch is highly extensible in that it has many custom extensions and it is
	 easier to implement them for both GPU and CPU versions of its code
	 [@fa18-523-57-PyTorch-tensorflow]. It can be extended using NumPy, Scipy
	 [@fa18-523-57-Scipy] and many other libraries
	 [@fa18-523-57-PyTorch-Extensions]. Examples on extending
	 PyTorch through Scipy and NumPy can be found at
	 [@fa18-523-57-PyTorch-Extensions]

## Drawbacks of PyTorch Over Existing Frameworks

When we compare PyTorch with its competitors, it looks like TensorFlow gives a
tight competition due to its use in other deep learning packages as well
[@fa18-523-57-competition]. TensorFlow has its advantages over PyTorch in
certain areas which are as below.

1. Coverage of functionality is less in PyTorch when compared to TensorFlow. The
	 functions like NumPy's flip along a dimension, checking NaN values, fast
	 fourier transformation are not readily available in PyTorch whereas these
	 functions and many higher functions are available in TensorFlow
	 [@fa18-523-57-PyTorch-tensorflow].

2. Serialization [@fa18-523-57-Serialization] can be defined as the process of
	 translating the input data into a format which can be easily transferred
	 across different platforms [@fa18-523-57-Serialization]. This capability in
	 TensorFlow is better than PyTorch that it even is capable of saving the
	 graphs can be saved as well. These graphs can easily be loading into
	 different languages like C++ and Java. This enables the deployments to not
	 depend on Python alone [@fa18-523-57-PyTorch-tensorflow].

3. Deployment is an activity which makes a code available to be used on a system
	 where the code is placed. Since the code developed in TensorFlow can be
	 easily saved in a format which can be used in different languages, TensorFlow
	 code can be easily deployed even in mobile applications
	 [@fa18-523-57-PyTorch-tensorflow].
