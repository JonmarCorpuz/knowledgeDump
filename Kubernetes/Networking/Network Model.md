# Kubernetes Network Model Overview

The [Kubernetes network mode](https://kubernetes.io/docs/concepts/services-networking/#the-kubernetes-network-model) defines how networking works between objects and external clients in a Kubernetes cluster

* Implemented through CNI plugins (*Calico*, *Cilium*, *etc.*)

<br>

# Network Model Pieces

## Pod Network

* Each pod in a cluster gets its own unique cluster-wide IP address 
* Handles communication between pods
* Ensures that all pods across the Kubernetes cluster can communicate with each other directly without the use of proxies or address translation

<br>

## Service API

* Provides a stable and long lived IP address or hostname for a service implemented by one or more backend pods
* Automatically