---
title: 'Clustering'
course: 'Azure AI Fundamentals'
date: 2026-02-04
topic: 'Machine Learning'
tags: [machine learning, AI, fundamentals]
---

# Lecture: Clustering

## Overview

**Clustering** is a form of unsupervised machine learning in which observations are grouped into clusters based on similarities in their data values, or features. This kind of machine learning is considered unsupervised because it doesn't make use of previously known label values to train a model. In a clustering model, the label is the cluster to which the observation is assigned, based only on its features.

## Detailed Notes

### Training a clustering model

Most commonly used algorithms is K-Means clustering, which consists of the following steps:

1. The feature (x) values are vectorized to define n-dimensional coordinates (where n is the number of features).

2. The number of clusters (k) is specified.

3. k initial centroids are randomly assigned within the n-dimensional feature space.

4. Each observation is assigned to the nearest centroid, forming k clusters.

5. The centroids are recalculated as the mean position of all observations in each cluster.

6. Steps 4 and 5 are repeated until the centroids no longer change significantly or a maximum number of iterations is reached.

### Evaluation a clustering model

- **Average distance to cluster center**: the average distance between each observation and the centroid of its assigned cluster. Lower values indicate more compact clusters.

- **Average distance to other center**: the average distance between each observation and the centroids of all other clusters. Higher values indicate better separation between clusters.

- **Maximum distance to cluster center**: the maximum distance between any observation and the centroid of its assigned cluster. Lower values indicate more compact clusters.

- **Sihouette**: a measure of how similar an observation is to its own cluster compared to other clusters. The silhouette score ranges from -1 to 1, where a value close to 1 indicates that the observation is well matched to its own cluster and poorly matched to neighboring clusters, a value of 0 indicates that the observation is on or very close to the decision boundary between two neighboring clusters, and negative values indicate that the observation may have been assigned to the wrong cluster.

## Resources

- [Lecture](https://learn.microsoft.com/en-us/training/modules/fundamentals-machine-learning/7-clustering?pivots=text)
- [K-Means Clustering](https://youtu.be/4b5d3muPQmA?si=UgYPPJNQoQGpRCj0)
