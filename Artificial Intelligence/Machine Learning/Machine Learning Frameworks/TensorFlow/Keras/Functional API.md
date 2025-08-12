# Keras Functional API Overview

The [Keras functional API](https://keras.io/guides/functional_api/) is a way to create models that are more flexible than the `keras.Sequential` API

* Can handle models with non-linear topology, shared layers, and multiple inputs and outputs
* Used as a way to build graphs of layers (The main idea is that a deep learning model is usually a Direct Acyclic Graph of layers)

<br>

Setup the Keras functional API
```Python
import numpy as np
import keras
from keras import layers
from keras import ops
```