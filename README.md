# Network Anomaly Detection

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Implementation](#implementation)
4. [Results](#results)
5. [Notebook](#notebook)

## Introduction
The goal of this project is to detect network anomalies for the [KDDCup99 dataset](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html). This project was a practical introduction to the use of clustering algorithms for anomaly detection. 

## Dataset
The [KDDCup99 dataset](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html) is the data set used for The Third International Knowledge Discovery and Data Mining Tools Competition, which was held in conjunction with KDD-99. It is also a labeled dataset, so we can use it to evaluate the performance of our clustering algorithms. The dataset contains 41 features. The features are a mix of categorical and numerical features. The dataset is highly imbalanced, with only a very small percentage of the data being labeled as an attack. 

## Implementation
We implemented the following clustering algorithms:
- K-Means
- Spectral Clustering
- DBSCAN 

For the clustering evaluation, we used the following matching algorithms:
- Hungarian Algorithm
- Purity based matching

We also used the following metrics to evaluate the performance of the clustering algorithms:
- Precision
- Recall
- F1-Score
- Accuracy

As for the categorical features, we used the following encoding techniques:
- One-Hot Encoding
- Label Encoding

## Results
The following table shows the results of the clustering algorithms. The results are shown for the different matching algorithms and metrics.

| Algorithm | Matching Algorithm | Precision | Recall | F1-Score | Accuracy | Conditional Entropy |
| --- | --- | --- | --- | --- | --- | --- |
| K-Means | Hungarian | 0.81 | 0.76 | 0.72 | 0.76 | 0.86 |
| K-Means | Purity | 0.81 | 0.72 | 0.65 | 0.72 | 0.86 |
| Spectral Clustering | Hungarian | 0.97 | 0.62 | 0.73 | 0.62 | 0.14 |
| Spectral Clustering | Purity | 0.97 | 0.62 | 0.73 | 0.62 | 0.14 |
| DBSCAN | Hungarian | 0.53 | 0.58 | 0.43 | 0.58 | 1.49 |
| DBSCAN | Purity | 0.53 | 0.58 | 0.43 | 0.58 | 1.49 |


## Notebook
The notebook for this project can be found [here](./Network-Anomaly-Detection.ipynb).

## Collaborators
- [Manar Amgad](https://github.com/manaramgadd)
- Ahmed Dusuki