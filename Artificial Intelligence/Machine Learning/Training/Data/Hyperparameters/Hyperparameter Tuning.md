# Hyperparameter Tuning Overview

* Model parameters are optimized ("tuned") by the training process itself (This works by running multiple trials of your training application with values for your chosen parameter)
* Your training application defines all the information that your model needs and you define the hyperparameters that you want to adjust while also targetting the variables that are used to evaluate each trial
* Optimizes target variables that you specify (Hyperparameter metrics)
* Users need to define the name and goal of each metric when configuring a hyperparameter tuning job (The goal specifies whether you want to tune your model to maximize or minimize the value of this metric)

<br>

# Hyperparameter Tuning Methods

A hyperparameter tuning method is a systematic approach used to find the best combination of hyperparameters for a machine learning model to optimize its performance

## Grid Search

A grid search constructs models for every possible configuration of those discrete hyperparameter values after data scientists establish every possible value for each hyperparameter (The constructed models are evaluated for performance and compared against each other resulting in the best model utilmately for training)

* Very comprehensive and exhaustive
* Inefficient and computationally resource-intensive although it does enable data scientists to consider all possible configurations in the hyperparameter space

<br>

## Randomized Search

A randomized search pulls samples from each range and constructs models for each combination of the statistical distributions for each hyperparameter provided by the user (Over the course of seeral iterations, the models are weighed against one another until the best model is found)

* Preferrable in situations where the hyperparameter search space contains large distributions
* Random search algorithms can return results comparable to grid search in considerably less time although it's not guaranteed to discover the most optimal hyperparameter configuration

<br>

## Bayesian Optimization

Bayesian optimization is a sequential model-based optimization (SMBO) algorithm that improves the sampling method of the next after each iteration of testing

* Probabilitically selects a new set of hyperparameter values that's likely to deliver better results (The probabilistic model is referred to as a surrogate of original objective function and the better the surrogate gets at predicting optimal hyperparameters the fast the process becomes with fewer objective function tests required)
* Far more efficient since no time is wasted on unsuitable combinations of hyperparameter values

<br>

## Hyperband

* Designed to improve on random search by truncating the use of training configurations that fail to deliver strong results while allocating more resources to positive configurations (This is achieved through successive halving which is a process that hittles down the pool of configurations by removing the worst-performing half after each round of training while the top 50% of each batch is carried into the next iteration until one optimal hyperparameter configuration remains)

<br>