# Overfitting Overview

[Overfitting](https://aws.amazon.com/what-is/overfitting/?nc1=h_ls) is an undesirable ML behavior that occurs when the machine learning model gives accurate predictions for training data but not for new data

* An overfit model can give inaccurate predictions and cannot perform well for all types of new data
* Occurs when the model cannot generalize and fits too closely to the training dataset instead

<br>

Potential root causes:
* The training data size is too small and doesn't contain enough data samples to accurately represent all possible input values
* The training data contains large amounts of irrelevant information (Noisy data)
* The model trains for too long on a single sample set of data
* The model complexity is high so it learns the noise within the training data

<br>

# Detecting Overfitting

* The best method to detect overfit models is by testing the machine learning models on more data with comprehensive representation of possible input data values and types 
* Usually part of the training data is used as test data to check for overfitting (A high error rate in the testing data indicates overfitting)

## K-Fold Cross-Validation

Cross-validation is when the training set is divided into K equally sized subsets or sample sets called folds

<br>

The training process consists of a series of iterations that each go through the following steps until the model is tested on every sample set:
1. Keep on subset as the validation data and train the machine learning model on the remaining K-1 subsets
2. Observe how the model performs on the validation sample
3. Score model performance based on output data quality

<br>

# Preventing Overfitting

* Overfitting can be prevented by diversifying and scaling your training data set or using some other data science strategies

## Early Stopping

Pausing the training phase before the model learns the noise in the data

* Getting the timing right is important or else the model will still not give accurate results

<br>

## Pruning

Identifying the most important features within a training set and eliminating the irrelevant ones (*You may prioritize face shape and ignore the shape of eyes when trying to predict if an image is an animal or human*)

<br>

## Regularization

A collection of training techniques that seek to reduce overfitting by grading features based on important in order to eliminate factors that don't impact the prediction outcomes

<br>

## Ensembling

Combines predictions from several separate machine learning algorithms