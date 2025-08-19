# Model Hyperparameter Overview

A model [hyperparameter](https://www.geeksforgeeks.org/machine-learning/difference-between-model-parameters-vs-hyperparameters/) is the parameter whose value is set before the model start training (Contains the data that govern the training process itself)

* Required for estimating the model parameters
* Estimated by hyperparameter tuning

<br>

# Hyperparameters

## Neural Network

| Neural Network Hyperparameter | Description |
| --- | --- |
| Learning rate | Sets the speed at which a model ajusts its parameters in each iteration (A high learning rate means that a model will adjust more quickly but at the risk of unstable performance and data drift while a low learning rate is more time-consuming and requires more data) |
| Learning rate decay | Sets the rate at which the learning rate of a network drops over time (The faster the rate the faster it allows the model to learn more quickly) |
| Batch size | Sets the amount of samples the model will compute before updating its parameter (A higher batch size weakens overall performnace but ajusting the learning rate along with batch size can mitigate this loss) |
| Number of hidden layers | Determines the depth which affects the model's complexity and learning ability (Fewer layers make for a simpler and faster model but more layers lead to better classification of input data) |
| Number of neurons per layer | Sets the width of the model (The more neurons per later the greater the breadth of the model and the better able it is to depict complext relationships between data points) |
| Momentum | The degree to which models update parameters in the same direction as previous iterations |
| Epochs | Sets the amount of times that a model is exposed to its entire training dataset during the training process (Greater exposure can lear to improved performance but runs the risk of overfitting) |
| Activation function | Allows a model to handle more complex datasets by introducing it to nonlinearity |

<br>

## SVM

| SVM Hyperparameter | Description |
| --- | --- |
| C | The ratio between the acceptable margin of error and the resulting number of errors when a model acts as a data classifier |
| kernel | A function that establishes the nature of the relationships between data points and separates them into groups accordingly |

<br>

## XGBoost Hyperparameters

| XGBoost Hyperparameter | Description |
| --- | --- |
| learning_rate | Controls the level of correction made during each round of training (Potential values range from 0 to 1 with 0.3 as the default) |
| n_estimators | Sets the number of trees in the model |
| max_depth | Determines the architecture of the decision tree by setting the maximum amount of nodes from the tree to each leaf which is the final classifier (MOre nodes lead to more nuanced data classification while smaller trees easily avoid overdrifting) |
| min_child_weight | The minimum weight needed to spawn a new tree (Lower minimum weights create more trees but with potential overfitting while larger weights recude complexity by requiring more data to split trees) |
| subsample | Sets the percentage of data samples used during each training round |


<br>

## Batch Size

* The total number of example to calculate Gradient in single iterations

<br>

### Mini-Batch SGD

## EPOD

* The full training pass over the entire training set