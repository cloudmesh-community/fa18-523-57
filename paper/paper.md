# PyTorch :hand: fa18-523-57

| Divya Rajendran
| divrajen@iu.edu
| Indiana University
| hid: fa18-523-57
| github: [:cloud:](https://github.com/cloudmesh-community/fa18-523-57/tree/master/paper)

* :o: this is a draft and therefore the review was halted

---

Keywords: Hid fa18-523-57, Machine Learning, Deep Learning, Deep Neural Nets, Python

---

## Abstract

The software industry has been increasingly adapting machine learning algorithms to make 
their machines intelligent and deep learning is a subset of machine learning which 
allows us to achieve a greater flexibility, capacity and computation power. To make it 
easier for the deep learning implementors, several frameworks which have the deep learning 
algorithms, in a less complex and easy to use format. PyTorch is one such deep learning 
framework which is in popular use due to its core language being python. This paper aims 
to introduce PyTorch and to enable users to install and start using PyTorch to work on some 
basic deep learning models or algorithms.


## Introduction

PyTorch [@paszke2017automatic] is a deep learning framework is built upon existing 
framework Torch, but written in Python. It has been developed the Artificial Intelligence
group at Facebook led by Adam Paszke, Soumith Chintala and team [@fa18-523-57-PyTorch-Wikipedia]. 
Torch was initially created for academic purposes and is extensively used for scientific 
computing in deep learning and machine learning currently. 

PyTorch can be used for faster computation of algorithms which are of expensive computations, 
and would allow the developers to make real time execution and analysis of algorithms and 
their results. Algorithms in Deep Learning and neural networks compute the peaks and descents 
of loss functions without using any pre-existing functions on gradient descent 
[@paszke2017automatic]. These algorithms would turn expensive based on the increasing number 
of iterations or relative calculations.

PyTorch performs faster calculations of complicated neural nets and other deep learning and 
artificial intelligence related algorithms making use of the combined power of Python and 
Torch. Since PyTorch is relatively simple owing to the use of Python as its base language and 
yet extremely powerful by making use of Torch, such computationally expensive algorithms are 
calculated faster using PyTorch and hence, it has been in popular use in the last few years 
even though it is relatively new.   


## Background

PyTorch as mentioned is a deep learning scientific framework which is completely written 
using Python. It is based of Torch [@fa18-523-57-Torch] which is wrapped in Lua, a programming 
language written in C. It runs even in constrained platforms through LuaJIT, a platform 
specific compiler. This platform specific compiler improves the performance of Torch as the 
underlying code would remain the same. 

By shedding Lua and LuaJIT, PyTorch came into existence by directly utilizing Python, 
increasing performance even further. It seamlessly integrates Python code and its related 
packages into PyTorch and builds all of its functionality in Python making Python an integral 
part of its design and thus becoming more popular with early developers.

Torch uses a function called Autograd which calculates the gradients of the loss function on 
its peaks and troughs. And Python has such an implementation too, a package called Autograd 
which is further adapted by PyTorch and uses a method called tape-based auto differentiation.
This technique basically works like a tape recorder by recording the gradients computed and 
by replaying these values in a reveres order. This functions implementation in PyTorch is 
much more faster as it combines the power of Python and Torch. [@fa18-523-57-PyTorch-Started]

Many developers have been using this library as an alternative to Numpy as it has taken 
advantage of GPU (Graphical Processing Unit) acceleration for faster computing 
[@fa18-523-57-PyTorch-Tensor]. And it mainly focusses on fastening the computational speed 
of numerical formulae related computations, which helps developer and data scientists alike 
to calculate extremely expensive code snippets to run in real time making use of the GPU. 
[@fa18-523-57-PyTorch-Tensor]


## Operations Using PyTorch

PyTorch has several inbuilt data structures which are widely used for deep learning and 
deep neural nets algorithms [@fa18-523-57-PyTorch-deep-learning].

1.	Tensors: PyTorch has a data structure names Tensors which works in close alignment to 
	Numpy arrays and also utilizing the GPU to speed up the calculation time on matrix 
	operations. 

2.	Computation Graph: In training a neural network, we often have to compute gradients 
	for every combination of weights and bias, which further needs to be updated using 
	gradient descent algorithms, here we utilize graphs to effectively compute the 
	gradients for every combination sequentially and train the neural network in the 
	process. This graph applies chain rule to compute all the gradients utilizing back 
	propagation method.


## Advantages of PyTorch

1.	Ramp Up Time for code execution for PyTorch is much faster than its competitor 
	TensorFlow, in that it uses dynamic creation of graphs rather than the static ones in 
	TensorFlow. Here, the compilation time for the code is much smaller for PyTorch and 
	the graph is built during run time, making it significantly faster than TensorFlow 
	[@fa18-523-57-PyTorch-tensorflow]. 

2.	Debugging in PyTorch is much easier when compared to TensorFlow as its underlying 
	language is Python, and debugging in Python is much more easier when compared to 
	TensorFlow code.

3.	Data Loading is much more faster in PyTorch as the APIs for loading the data are 
	designed in a manner to best utilize its parallelizing data loading capability. 

4.	PyTorch is highly extensible in that it has many custom extensions and it is easier to 
	implement them for both GPU and CPU versions of its code.
	
5.	PyTorch also avoids using static graphs which are used in TensorFlow and instead builds 
	graphs dynamically using a much faster implementation of reverse mode tape-based auto 
	differentiation. [@fa18-523-57-PyTorch-Started]
	
	
## Implementation

If you have never used PyTorch before you need to install PyTorch, check https://pytorch.org 
for more instructions on the system requirements and different ways to install PyTorch. 
[@fa18-523-57-PyTorch-installation]

In terminal or command prompt, enter the below line to install the PyTorch library.

pip install torch torchvision

![installation](images/install.png){#fig:installation}

## Conclusion

PyTorch is a great framework which reduces the time taken to compute various gradient 
descents and the underlying calculations for neural networks and is sure to be in much 
more use than we see now.
