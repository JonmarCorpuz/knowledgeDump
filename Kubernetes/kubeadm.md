# kubeadm Overview

`kubeadm` is a Kubernetes tool that simplifies the process of setting up and managing Kubernetes clusters

* Provides the necessary tools to create a functional Kubernetes cluster with minimal complexity
* Handles Kubernetes version upgrades seamlessly
* Abstracts away the complexities involved in manually setting up a Kubernetes cluster (Makes it accessible for users with less experience in managing distributed systems)
* Well supported by the community

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# kubeadm Operations

* `kubeadm init` sets up the Kubernetes control plane nodes and configures the necessary Kubernetes components (*API Server*, *Controller Manager*, *Scheduler*, *etc.*)
* `kubeadm join` joins any additional nodes to the Kubernetes cluster as worker nodes by connecting them to the control plane
