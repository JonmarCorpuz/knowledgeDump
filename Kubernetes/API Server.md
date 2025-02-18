# API Server Overview

The API server in Kubernetes is a component in the control plane that acts as the gateway through which all internal and external communications pass to interact with the cluster by exposing the Kubernetes API to external resources (Serves as the central mechanism for managing a Kubernetes cluster's state)

* Allows users, services, and other components to communicate and manipulate Kubernetes resources and workloads
* Processes all REST requests to the Kubernetes cluster (*Via kubectl*, *Via internal components*, *Via external applications*, *etc.*)
* Interfaces directly with etcd in order to ensure that the state of all Kubernetes objects is persistent and consistent
* Authenticates each request to verify the identity of the requester and that they're authorized to perform the action that they're requesting
* Before completing any action, the API server processes the request through various configurable admission controllers that can modify or reject requests to enforce specific governance rules (*Resource limits*, *Security policies*, *etc.*)
* Validates requests against the Kubernetes schema to ensure they're correct before executing them (If the request is valid, the API server changes the state of resources in etcd or triggers controllers to manage the state as required)
* 

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

