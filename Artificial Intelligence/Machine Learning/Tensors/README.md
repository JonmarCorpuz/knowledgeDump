# Tensor Overview

A [tensor](https://machinelearningmastery.com/introduction-to-tensors-for-machine-learning/) is a generalization of vectors and matrices 

* Easily understood as a multidimensional array

<br>

Example of a three-dimensional 3x3x3 tensor as a NumPy ndarray
```Python
# Create tensor
from numpy import array

T = array([
  [[1,2,3],    [4,5,6],    [7,8,9]],
  [[11,12,13], [14,15,16], [17,18,19]],
  [[21,22,23], [24,25,26], [27,28,29]],
  ])
print(T.shape)
print(T)
```