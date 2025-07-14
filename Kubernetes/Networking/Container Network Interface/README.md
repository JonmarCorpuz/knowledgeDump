# CNI Overview

The Container Network Interface is a specification and a set of plugins that handles network connectivity for containers in a Kubernetes cluster

* Required to implement the [Kubernetes network model](https://kubernetes.io/docs/concepts/services-networking/#the-kubernetes-network-model)
* Responsible for assigning an IP address to a newly created pod
* Sets up the network namespace so the pod can communicate with other components of the Kubernetes cluster
* Configures routing so pods across nodes can reach each other
* Optionally enforces network policies