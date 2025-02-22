# Neural Network from Scratch on MNIST

## Overview

In this project I built a neural network from scratch—without relying on high-level machine learning libraries—using the MNIST dataset. 
The implementation includes:
- Layer classes
- forward pass
- gradient functions for backpropagation
- Various gradient descent methods including full batch, mini-batch, and stochastic gradient descent

## Motivation

The primary motivations for building this neural network from scratch were: 
- Demonstrate my understanding of the fundamental mathematics behind neural networks
- Building everything from scratch provides hands-on experience with core concepts such as forward propagation, backpropagation, and parameter updates
- MNIST is a well-known benchmark in ML and DL
  
## Approach

The development of the neural network involved several key steps:

### 1. Building Layer Classes
- Each layer (e.g., Dense layer, activation layer) is implemented as its own class. This modular design makes the network easier to understand, maintain, and extend  
- Each layer holds its own parameters (weights and biases) and implements a `forward` method to compute its output given an input
  
### 2. Forward Pass and Loss Computation

- **Forward Propagation:**  
  Data is passed through the network using `forward` methods, outputing class probabilities.
  
- **Loss Function:**
  Categorical Cross-Entropy Loss:  Computed by comparing the network's output with the one-hot encoded true labels.

### 3. Backpropagation and Gradient Derivation

- **Gradient Computation:**  
  Gradients of the loss function with respect to each layer's parameters were derived manually (chain rule through each layer)
  
- **Backpropagation Process:**  
  Starting from the output layer, the gradient is propagated backward through the network. Each layer's `backward` method computes the gradient with respect to its input and parameters.
  
- **Parameter Update:**  
  Update the network weights and biases using gradient descent (full batch, mini batch and SGD)

### 4. Gradient Descent Variants

Three optimization strategies were implemented:

- **Full-Batch Gradient Descent:**  
  Computes the gradient over the entire dataset for each update

- **Mini-Batch Gradient Descent:**  
  Divides the dataset into smaller batches and computes gradients on each mini-batch

- **Stochastic Gradient Descent (SGD):**  
  Updates parameters using the gradient from a single training sample at a time. SGD introduces a high level of noise in the updates, which can be beneficial for escaping local minima
  
## Summary

This project demonstrates the fundamentals of neural networks, provides a hands-on approach to understanding the math behind networks
