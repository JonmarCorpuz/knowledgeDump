# Non-Linear Activation Function Overview

<br>

# Non-Linear Activation Functions

## Rectified Linear Unit

ReLU is 

* Outputs the input directly if it's positive otherwise it outputs zero
* Allows NNs to learn complex patterns while remaining computationally efficient by introducing non-linearity to the model
* Helps resolve the vanishing gradient problem
* Improves efficiency by having only some neurons activate at any time (Sparse activation)
* Allows faster training due to better gradient behavior
* Neurons can get stuck outputting zero and make it become inactive and not learn further (**Dying ReLU**)

<br>

Mathematically describe as
```Text
f(x)=max(0,x)
```

* *x* is the input to the neuron(If **X > 0** then the output is **x** and if **x < 0** then the output is **0**)