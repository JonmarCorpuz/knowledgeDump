# AI/ML Model Overview

* Data driven
* We can have a clean set of data or a clean AI model but we cannot learn anything from garbage results (Garbage-in garbage-out)

<br>

Classification models
* Logistic regression
* Decision trees
* Random forest
* Naive Bayes
* etc.

<br>

Dimensionality reduction models
* PCA (Unsupervised technique used primarily for dimensionality reduction)
* Robust rolling PCA (R2-PCA)
* Kernel PCA
* ICA
* autoencoder

<br>

Clustering
* K-means
* Robust rolling K-means (R2K-means)
* Density-based spatial clustering of applications with noise (DBSCAN)
* Gaussian mixture model

<br>

Solving equations (Explicit/Implicit replication)
* Mapping input data to labels via FNNs (Supervised)
* Using a neural network as a solution (Unsupervised)

<br>

Image classification
* CNNs

<br>

Sequence analysis (*Sentiment analysis*, *etc.*)
* RNNs
* LSTMs
* GRUs

<br>

LLMs (*Sentiment analysis*, *Mathematical reasoning*, *etc.*)
* Transformers

<br>

Sampling models (*Simulating/generating data preserving stylized facts*, *etc.*)
* MCMC (Parametric)
* GANs (Non-parametric)

<br>

* Try different AI models on various simulated data and compare the results
* Check robustness by adding noise
* Check the consistency between in-sample vs out-sample

<br>

A few questions on AI-based models
```Text
Q: Can it be understood by humans or is it simply a black box?
Q: If the model doesn't do well, do we know why?
Q: Can we understand or follow the model prediction/decision?
Q: When do we know a trained model has failed?
Q: How robust is the model against the adversarial attack?
```
