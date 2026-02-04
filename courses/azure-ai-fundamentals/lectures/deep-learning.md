---
title: 'Deep Learning'
course: 'Azure AI Fundamentals'
date: 2026-02-04
topic: 'Machine Learning'
tags: [machine learning, AI, fundamentals]
---

# Lecture: Deep Learning

## Overview

**Deep learning** is a subset of machine learning that uses neural networks with many layers (hence "deep") to model complex patterns in data. Deep learning models are particularly effective for tasks such as image and speech recognition, natural language processing, and other applications that require understanding high-dimensional data.

## Detailed Notes

### How does a neural network learn?

1. The training and validation datasets are defined, and the training features are fed into the input layer.

2. Each neuron in the hidden layers applies a weighted sum of its inputs, adds a bias term, and passes the result through an activation function to introduce non-linearity.

3. The output layer produces the final predictions based on the activations from the last hidden layer.

4. The loss function calculates the difference between the predicted outputs and the actual labels in the training data.

5. An optimization algorithm, such as stochastic gradient descent or Adam, is used to adjust the weights and biases in the network to minimize the loss.

6. The changes are propagated back through the network using backpropagation, updating the weights and biases in each layer.

7. Steps 2-6 are repeated for multiple epochs until the model converges or reaches a satisfactory level of performance.

## Resources

- [Lecture](https://learn.microsoft.com/en-us/training/modules/fundamentals-machine-learning/7-clustering?pivots=text)
- [Neural networks](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi)
