# Neural Network Overview

* Decisions are based on current data
* We try to mimic the human brain (We take an input and we want to process those input by different parameters and weights in it in order to try to find the relationship between those parameters)
* We take multiple inputs fed into a layer of neuron network blocks

<br>

# Activation Function

* Used in the hidden layer (*ReLU*, *Only RNN recommended for Sigmoid or TanH*) and the output layer (*Linear regression*, *Sigmoid for binary and multilabel classification*, *Softmax for multi classification*, *etc.*)

<br>

## Rectified Linear Unit (ReLU)

* It has positive value when x is positive 
* It's always zero if x is below zero

<br>

```Python
y = max(0.0,x)
```

<br>

## Hyperbolic Tangent (TanH)

* Takes an input and output range from -1 to 1

<br>

```Python
y = (exp(x) - exp(-x)) / (exp(x) + exp(-x))
```

<br>

## Logistic Function (Sigmoid)

* It takes an input and output range from 0 to 1

<br>

```Python
y = 1.0 / (1.0 + exp(-x))
```

<br>

## Softmax

```Python
y = exp(x) / exp(x).sum()
```