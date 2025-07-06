# Namespace Overview

* A namespace is a Kubernetes object that provides logical isolation for other Kubernetes objects within a Kubernetes cluster

* Allows cluster resources to be divided between multiple users 
* Resource limits can be applied to specific namespaces
* Resources within the same namespace can refer to each other simply by using their hostnames (The namespace must be appended to the hostname in order to do this)

<br>

# Kubernetes Namespaces

## Default

<br>

## kube-system

<br>

## kube-public

<br>

## Custom

<br>

# DNS Entries

```Bash
# Hostname
SERVICE_NAME.NAMESPACE.svc.cluster.local

# svc refers to Service
# cluster.local refers to the local domain
```