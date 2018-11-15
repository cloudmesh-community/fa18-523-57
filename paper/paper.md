# PyTorch :hand: fa18-523-57

| Divya Rajendran
| divrajen@iu.edu
| Indiana University
| hid: fa18-523-57
| github: [:cloud:](https://github.com/cloudmesh-community/fa18-523-57/tree/master/paper)

* :o: language can be improved. Sentences are incomplete and words are missing
* :o: not following markdown or FAQs we posted on how to use urls so i correctd this

---

Keywords: Hid fa18-523-57, Deep Learning, gradient descents, Autograd, neural networks, Python

---


:o: remove the abstract and introduce into the introduction. This paper is too short to justify an abstract
:o: start with pytorch not whit a scnario, 

The software industry has been increasingly adapting machine learning algorithms to make their machines intelligent and deep learning is a subset of machine learning which allows us to achieve a greater flexibility, capacity and computation power. 
:o: unclear

To make it easier for the deep learning implementors, several frameworks  which have the deep learning algorithms, in a less complex and easy to use format. :grammar:

PyTorch is one such deep learning framework which is in popular use due to its core language being python. This paper aims to introduce PyTorch and to enable users to understand the role PyTorch plays in faster implementation of Deep Learning algorithms. :o: if there is one, you must liste the others with citations. As you remove the abstract you can now do that


:o: grammar errors just indicated with :o: at the end of sentence

PyTorch [@paszke2017automatic] is a deep learning framework is built upon existing framework Torch, but written in Python.  :o:

It has been developed the Artificial Intelligence group at Facebook ~~led by Adam Paszke, Soumith Chintala and team
:o: no need to name them does not help to understand what PyTorch is.~~

[@fa18-523-57-PyTorch-Wikipedia]. Torch was initially created for academic purposes and is extensively used for scientific computing in deep learning and machine learning currently. :o: :o: citations missing

PyTorch can be used for faster computation of algorithms which are of expensive computations, :o: and would allow the developers to make real time execution and analysis of algorithms and their results. :o: Algorithms in Deep Learning and neural networks compute the peaks and descents of loss functions without using any pre-existing functions on gradient descent [@paszke2017automatic]. :o: These algorithms would :o: turn expensive based on the increasing number of iterations or relative calculations. :o:

PyTorch performs faster :o: faster tahn what :o: calculations of complicated neural nets and other deep learning and artificial intelligence related algorithms making use of the combined power of Python and Torch. Since PyTorch is relatively simple owing :o: the use of Python as its base language and yet extremely powerful by making use of Torch :o: cite missing :o: this can not b understood as i now need to knwo what torkh is so you need to explain thst :o:, such :o: which: computationally expensive algorithms are calculated faster using PyTorch and hence, it has been in popular use :o: in the last few years even though it is relatively new.   


## Background

PyTorch ~~as mentioned~~ is a deep learning scientific framework which is ~~completely~~ written using Python. It is based of Torch [@fa18-523-57-Torch] which is wrapped in Lua, a programming language written in C. It runs even in constrained platforms through LuaJIT, a platform specific compiler. This platform specific compiler improves the performance of Torch as the underlying code would remain the same. 

By shedding :o: Lua and LuaJIT, PyTorch came into existence by directly utilizing Python, increasing performance even further :o: than what? :o:. It seamlessly integrates Python code and its related packages into PyTorch and builds all of its functionality in Python making Python an integral part of its design and thus becoming more popular with early developers.

Torch uses a function called Autograd which calculates the gradients of the loss function on its peaks and troughs. And Python has such an implementation too, a package called Autograd which is further adapted by PyTorch and uses a method called tape-based auto differentiation. This technique basically works like a tape recorder by recording the gradients computed and by replaying these values in a reveres order. This functions implementation in PyTorch is much more faster as it combines the power of Python and Torch. [@fa18-523-57-PyTorch-Started]

Many developers have been using this library as an alternative to Numpy as it has taken advantage of GPU (Graphical Processing Unit) acceleration for faster computing [@fa18-523-57-PyTorch-Tensor]. And :o: it mainly focusses on fastening :o: the computational speed of numerical formulae related computations, which helps developer :o: and data scientists alike to calculate extremely expensive code snippets to run in real time making use of the GPU [@fa18-523-57-PyTorch-Tensor].


## Getting Started

If you have never used PyTorch before you need to install PyTorch, check <https://pytorch.org> for more instructions on the system requirements and different ways to install PyTorch [@fa18-523-57-PyTorch-installation].

In :o: terminal or command prompt, enter the below line to install the PyTorch library.

```python
pip install torch torchvision
```

:o: Remove the image and replace with ascii text

![installation](images/install.png){fig:installation}

Sample tensor initialization can be seen below:

:o: Remove the image and replace with ascii text

![installation](images/Initialization.png){fig:Initialization}

~~For~~ step by step instructions for using PyTorch can be found at <https://pytorch.org/tutorials/index.html>. There are several tutorials to use PyTorch on Deep Learning Algorithms with downloadable code, which can be used to learn how to use the library. :o: than name them?


## Operations Using PyTorch

PyTorch has several inbuilt data structures which are widely used for deep learning and deep neural nets algorithms [@fa18-523-57-PyTorch-deep-learning]. These are:

1. Tensors: ~~PyTorch has a data structure names~~ Tensors are ... and work in close alignment to Numpy arrays and also utilizing the GPU to speed up the calculation time on matrix operations. :o: does not explain what tensors are

2. Computation Graph: In training a neural network, we often have to compute gradients for every combination of weights and bias, which further needs to be updated using gradient descent algorithms, here we utilize graphs to effectively compute the gradients for every combination sequentially and train the neural network in the process. This graph applies :o: chain rule to compute all the gradients utilizing back propagation method.


## Implementation

When using PyTorch, we need to import it as is seen in the Installation image :o:. To use the auto differentiation technique we discussed above :o: you dod not discuss in detail so i do not understand, we use the library *torch.autograd*. Using this library we can compute the gradients for the peaks and troughs of the loss function  [@fa18-523-57-PyTorch-modules]. We use this library to train weights for neural networks through a process called backward pass. :o: I do not understand

To build neural networks we use the  library called *torch.nn*. We use the function *torch.nn.Sequential* to initialise a model with a linear stack of layers and use *torch.nn.MSELoss()* to initialise the loss function, which measures the mean squared error between the input and ouput layers [@fa18-523-57-PyTorch-modules]. Using the *torch.optim* package we can define our optimizer which updates the weights. This package abstracts the optimization algorithm and provides pre-existing optimization algorithms like Adam, AdaGrad and so on [@fa18-523-57-PyTorch-modules]. :o: doe snot explain what is done, I do not understand what is done.

For greater detail :o: basically the previous text is confusing, so the reader must go to the original? :o: version of the implementation please follow the step by step tutorial at <https://github.com/yunjey/pytorch-tutorial>. It has a tutorial for three levels of developers, a beginner level, an intermediate level and an advanced level, which is extremely helpful for new developers.


## Advantages of PyTorch Over Existing Frameworks

1. Ramp Up Time :o: what is that for code execution for PyTorch is much faster than its competitor TensorFlow, in that it uses dynamic creation of graphs rather than the static ones in TensorFlow. Here, the compilation time for the code is much smaller for PyTorch and the graph is built during run time, making it significantly faster than TensorFlow [@fa18-523-57-PyTorch-tensorflow]. 

2. Debugging in PyTorch is easier when compared to TensorFlow as it's underlying language is Python, and debugging in Python is much easier when compared to TensorFlow code. :o:

3. Data Loading is much ~~more~~ faster in PyTorch as the APIs for loading the data are designed in a manner to best utilize its parallelizing data loading capability. 

4. PyTorch is highly extensible in that it has many custom extensions :o: citeation :o: and it is easier to implement them for both GPU and CPU versions of its code.
	
5. PyTorch also avoids using static graphs :o: already mentioned :o: which are used in TensorFlow and instead builds graphs dynamically using a much faster implementation of reverse mode tape-based auto differentiation. [@fa18-523-57-PyTorch-Started]


~~Conclusion~~

PyTorch is a great framework which reduces the time taken to compute various gradient descents and the underlying calculations for neural networks and is sure to be in much more use than we see now. :o: speculation :o: citation missing :o:
