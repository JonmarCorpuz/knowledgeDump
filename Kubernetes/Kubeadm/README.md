# Kubeadm Overview

* Helps set up a multi-node cluster using Kubernetes best practices
* Requires a master node and some worker nodes
* Requires a container runtime and the kubeadm tool installed
* Requires the pod network to be set up before joining the worker nodes to the master node
* All the control plane components run as a pod or a deployment within the Kubernetes cluster