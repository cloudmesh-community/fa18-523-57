---
title: "Caffe - A Deep Learning Framework (Draft)"
date: "October 2018"
author: "Pramod Duvvuri, Indiana University"
---

## Abstract
The amount of data generated has increased exponentially and so did the advancement of computing power, both these have led us to the era of deep learning. This paper aims to summarize a deep learning framework knows as Caffe which was developed by a post-doc named Yangqing Jia at University of California, Berkeley in 2013. It is written in C++ and is known for it fast execution and it's Python interface allows it to be used by the vast majority of Python users. The framework has then been open-sourced, allowing many users to use, develop and contribute to improve the framework.

## Keywords
fa18-523-58, Deep Learning, Python, C++

## Introduction
The deep learning revolution has led to the need for state-of-the-art implementations of Artificial Neural Network (ANN) architectures. These architectures are too hard to code from scratch for most people who understood them conceptually and needed implementation to use them to solve specific problems. The first deep learning framework to gain popularity was Theano. Theano was developed at the University of Montreal in 2007. It was primarily used by the academic researchers at the university. Theano was built using Python which essentially made it slower for larger models, for production grade models speed is imperative. This meant there was need for a new popular and fast deep learning framework, especially in computer vision. Caffe was built using C++ and this made it very fast and ideally suitable for deployment in production. Caffe at the time of public release or open sourcing had the best implementation of Convolutional Neural Network (CNN) which are primarily used in solving computer vision problems. This made all the vision researchers adopt Caffe.

## Architecture
The Caffe architecture mainly consists of layers or it had layer wise design all designed and built using C++. This architecture at the time of Caffe creation was considered really good but since then newer deep learning framework's such as Tensorflow which was created by Google had a more flexible design. This flexible design is with respect to the various nodes in the ANN, since ANNs are primarily consisted of layers and each layer has multiple nodes. The ability to flexibly desing these nodes was very important to the researchers since this helped them achieve higher accuracy rates for model benchmarking.

## Use Cases
The Caffe framework was primarily used by the computer vision research community. As mentioned above, it had the fastest and the best implementation of the CNN. Two use cases of the usage of Caffe to tackle a notorious computer vision problem shall be included in this section. This might help the reader to identify why it is so prominent among computer vision researchers.

## Conclusion
Caffe helped the data science community make valuable contributions to research with its fast execution times. All the latest deep learning frameworks have referred to the implementation style of the CNN in Caffe. Caffe2 was a project that was started at Facebook after the success of Caffe. PyTorch is another popular deep learning framework recently which was developed at Facebook and had dynamic graph computational ability which was lacking in tensorflow. PyTorch was received very well by the community. By the end of March 2018, Caffe2 was merged with PyTorch by Facebook. These days the choice of a deep learning framework when you have huge amounts of data is a two way battle between PyTorch and Tensorflow. Both Google and Facebook constantly keep updating these frameworks from the feedback they receive from the developer community.

## Acknowledgements
The author would like to thank Professor Gregor Von Laszewski for providing this opportunity to work on this paper summary.

## References
