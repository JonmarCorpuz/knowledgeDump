# API Server Overview

The API server in Kubernetes is a component in the control plane that acts as the gateway through which all internal and external communications pass to interact with the cluster by exposing the Kubernetes API to external resources 

* Allows users, services, and other components to communicate and manipulate Kubernetes resources and workloads
* Processes all REST requests to the Kubernetes cluster (*Via kubectl*, *Via internal components*, *Via external applications*, *etc.*)
* Interfaces directly with etcd in order to ensure that the state of all Kubernetes objects is persistent and consistent
* Ensures that requests are made by verified entities by handling authentication of users and nodes
* Enforces authorization policies to control what actions users and services can perform

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

