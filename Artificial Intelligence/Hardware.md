# tmp

<br>

* CPU, GPU, TPU, Edge devices

<br>

# CPU

* Quick prototyping that requires maximum flexibility
* Simple models that don't take long to train
* Small models with small and effective batch sizes
* Models that contain many custom TensorFlow operations written in C++
* Models that are limited by available I/O or the networking bandwidth of the host system

<br>

```Text
Input --> [Control, ALU, Memory] --> Output
```

<br>

L2 Memory

```Text
Input --> ([Control, ALU, Memory], [Control, ALU, Memory], [L2 Memory]) --> Output
```

<br>

4 core CPU

```Text
Input --> {([Control, ALU, Memory], [Control, ALU, Memory], [L2 Memory]), ([Control, ALU, Memory], [Control, ALU, Memory], [L2 Memory]), ([Control, ALU, Memory], [Control, ALU, Memory], [L2 Memory]), ([Control, ALU, Memory], [Control, ALU, Memory], [L2 Memory]), [L3 Memory]} --> Output
```

* Higher cost per core

<br>

# GPU

* Capable of processing arrays of pixels
* Models with a significant number of custom TF/PyTorch/JAX operations that must run at least partially on CPUs
* Models with TF ops that are not available on Cloud TPU
* Mdeium-to-large models with larger effective batch sizes

```Text

```

<br>

# TPU

* Enables specialized Matrix calculations
* Models dominated by matrix computations
* Models with no custom TF/PyTorch/JAX operations inside the main training loop
* Models that train for weeks or months
* Large models with large effective batch sizes

<br>

## Cloud TPUs

* Not suitable for certain workloads (*Linear algebra programs that require frequent branching or contain many element-wise algebra operations*, *Workloads that access memory in a sparse manner*, *Workloads that require high-precision arithmetic*, *Neural network workloads that contain custom operations in the main training loop*, *etc.*)

<br>

## HBM Memory