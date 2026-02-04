---
title: 'Multiclass Classification'
course: 'Azure AI Fundamentals'
date: 2026-02-03
topic: 'Machine Learning'
tags: [machine learning, AI, fundamentals]
---

# Lecture: Multiclass Classification

## Overview

**Multiclass classification** is used to predict to which of multiple possible classes an observation belongs. As a supervised machine learning technique, it follows the same iterative train, validate, and evaluate process as regression and binary classification in which a subset of the training data is held back to validate the trained model.

## Detailed Notes

To train a multiclass classification model, we need to use an algorithm to fit the training data to a function that calculates a probability value for each possible class.

### One-vs-Rest (OvR) algorithms

One-vs-Rest (OvR), also known as One-vs-All (OvA), is a common strategy for extending binary classification algorithms to handle multiclass classification problems. In this approach, a separate binary classifier is trained for each class in the dataset. Each classifier learns to distinguish between one specific class and all other classes combined. During prediction, each classifier outputs a probability score indicating the likelihood that the input belongs to its respective class. The class with the highest probability score is then selected as the final prediction.

f_i(x) = P(class_i|x) for i = 1, 2, ..., n

### Multinomial algorithms

Multinomial algorithms are designed to handle multiclass classification problems directly, without the need to decompose them into multiple binary classification tasks. These algorithms can simultaneously consider all classes during the training process, allowing them to learn the relationships between features and multiple classes more effectively. Examples of multinomial algorithms include multinomial logistic regression and certain types of decision trees and neural networks that are inherently capable of multiclass classification.

f(x) = [P(class_1|x), P(class_2|x), ..., P(class_n|x)]

Where P(class_i|x) represents the probability of the input x belonging to class i.

### Evaluation Metrics

You can evaluate a multiclass classifier by calculating binary classification metrics for each individual class. Alternatively, you can calculate aggregate metrics that take all classes into account.

## Resources

- [Lecture](https://learn.microsoft.com/en-us/training/modules/fundamentals-machine-learning/6-multiclass-classification?pivots=text)
