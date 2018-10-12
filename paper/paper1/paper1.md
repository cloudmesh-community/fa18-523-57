# PyTorch (draft)

## Abstract:

Even though PyTorch is still in its early years, many developers and data scientists are adapting this framework to utilize the enormous computational capacity it offers. Due to its ease of use many new developers prefer PyTorch. It also avoids using static graphs which are used in TensorFlow and instead builds graphs dynamically using a much faster implementation of reverse mode tape-based auto differentiation. It seamlessly integrates Python code and its related packages into PyTorch and builds all of its functionality in Python making Python an integral part of its design and thus becoming more popular with early developers.


## Keywords:

Hid fa18-523-57, Machine Learning, Deep Learning, Deep Neural Nets, NLP


## Introduction :

Before describing what PyTorch is and what it does, it is good to know about Torch and its capabilities. Torch was initially created for academic purposes and is extensively used for scientific computing in deep learning and machine learning. Algorithms in Deep Learning and neural networks compute the peaks and descents of loss functions without using any pre-existing functions on gradient descent[@paszke2017automatic]. To fasten the computation of the above values Python uses technique called tape-based auto differentiation which basically  works like a tape recorder. This technique records the gradients computed and replays them in a reverse order, which further led to the creation of Torch which extensively utilized the Autograd package in Python. Many have used this library as an alternative to Numpy as it has taken advantage of GPU acceleration for faster computing[@fa18-523-57-PyTorch-Tensor].

Torch is wrapped in Lua a programming language which is written in C and runs even in constrained platforms. It has LuaJIT a platform specific compiler which improves the performance of Torch. Shedding Lua and LuaJIT, PyTorch came into existence  directly utilizing Python increasing performance even further. It has been in popular use in the last few years due to its increasingly powerful and simple structure to implement complicated neural nets. PyTorch, mainly focusses on fastening the computational speed of numerical formulae related computations, which helped developer and data scientists alike to calculate extremely expensive code snippets to run in real time making use of the GPU[@fa18-523-57-PyTorch-Tensor].

Even though PyTorch is still in its early years, many developers and data scientists are adapting this framework to utilize the enormous computational capacity it offers. Due to its ease of use many new developers prefer PyTorch. It also avoids using static graphs which are used in TensorFlow and instead builds graphs dynamically using a much faster implementation of reverse mode tape-based auto differentiation. It seamlessly integrates Python code and its related packages into PyTorch and builds all of its functionality in Python making Python an integral part of its design and thus becoming more popular with early developers [@fa18-523-57-PyTorch-Started].


## Implementation:

Will be added soon.


## Operations Using PyTorch:

PyTorch has several inbuilt data structures which are widely used for deep learning and deep neural nets algorithms [@fa18-523-57-PyTorch-deep-learning].

1.	Tensors: PyTorch has a data structure names Tensors which works in close alignment to Numpy arrays and also utilizing the GPU to speed up the calculation time on matrix operations. 

2.	Computation Graph: In training a neural network, we often have to compute gradients for every combination of weights and bias, which further needs to be updated using gradient descent algorithms, here we utilize graphs to effectively compute the gradients for every combination sequentially and train the neural network in the process. This graph applies chain rule to compute all the gradients utilizing back propagation method.


## Advantages of PyTorch:

1.	Ramp Up Time for code execution for PyTorch is much faster than its competitor TensorFlow, in that it uses dynamic creation of graphs rather than the static ones in TensorFlow. Here, the compilation time for the code is much smaller for PyTorch and the graph is built during run time, making it significantly faster than TensorFlow [@fa18-523-57-PyTorch-tensorflow]. 

2.	Debugging in PyTorch is much easier when compared to TensorFlow as its underlying language is Python, and debugging in Python is much more easier when compared to TensorFlow code.

3.	Data Loading is much more faster in PyTorch as the APIs for loading the data are designed in a manner to best utilize its parallelizing data loading capability. 

4.	PyTorch has many custom extensions and easier to implement them for both GPU and CPU version of its code.


## Conclusion:

PyTorch is a great framework which reduces the time taken to compute various gradient descents and the underlying calculations for neural networks and is sure to be in much more use than we see now.
