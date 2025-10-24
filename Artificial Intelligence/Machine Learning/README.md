# Machine Learning Overview

[ML](https://cloud.google.com/learn/what-is-machine-learning?hl=en) is a subset of AI that enables machines to autonomously learn and improve using neural networks and deep learning without being explicitly programmed and by feeding it large amounts of data

* Allows computer systems to continuously adjust and enhance themselves as they accrue more experiences (The performance can be improved by providing larger and more varied datasets to be processed)

<br>

Machine learning process
```Text
Problem Definition --> Data Identification (Feature Engineering) --> Data Preparation (Feature Engineering) --> Define Model --> Hyperparameter --> Train and Evaluate --> Save and Deploy for Serving --> Serving (Prediction)
```

<br>

The success of ML, DL, and LLMs is more due to 
* Availability of data (Big data)
* Availability of more powerful computational engines (*GPUs*, *TPUs*, *NPUs*, *etc.*)
* Quantum computing

<br>

`Inputs * Weights + Bias = Prediction`

# Floating Point Operations per Second (FLOPs)

| | | | |
| --- | --- | --- | --- |
| 1952 | Estimating the entropy of English | kiloFLOPs | |
| 1979 | Speech recognition | gigaFLOPs | |
| 1994 | Machine translation | teraFLOPs | |
| 2020 | Language understanding | yottaFLOPs | |
| 2025 | xxxGPT | quettaFLOPs | |

<br>

# Types of Machine Learning

```Text
Machine Learning
|---> Supervised |------> Classification
|                |------> Regression
|
|---> Unsupervised |----> Clustering
|
|---> Deep Learning |---> Generative AI
```

## Supervised 

* Deals with labeled data
* Task driven

<br>

| Supervised Learning Type | Description | ML Model | Example |
| --- | --- | --- | --- |
| Classification | Predicts a categorical variable | Logistic regression | *Determining whether a picture shows a cat or a dog* |
| Regression | Predicts a numeric variable | Linear regression | *Forecasting sales for a product based on its past sales* |

<br>

## Unsupervised

* Deals with unlabeled data
* Data-driven 
* Identifies a pattern

<br>

| Unsupervised Learning Type | Description | Learning Model/Technique | Example |
| --- | --- | --- | --- |
| Clustering | Groups data points together | k-means clustering | *Using customer demographics to determine customer segmentation* |
| Association | Identifies underlying relationships | Association rule learning | *Correlating two products to place them closer in a grocery store* |
| Dimensionality Reduction | Reduces the number of dimensions | Principal component analysis | *Combining characteristics to create a simplified rule for an insurance quote* |