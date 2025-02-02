# Config Connector Overview

[Config Connector](https://cloud.google.com/config-connector/docs/overview) is an open-source Kubernetes add-on that lets users manage their Google Cloud resources through Kubernetes

* Provides a collection of Kubernetes [Custom Resource Definitions](https://kubernetes.io/docs/concepts/extend-kubernetes/api-extension/custom-resources/) and controllers

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Customer Resource Definition

* Allows Kubernetes to create and manage Google Cloud resources when users configure and apply Objects to their cluster
* For Config Connector CRDs to function correctly, Config Connector deploys Pods to your Nodes that have elevated RBAC permissions (The create, delete, get, and list permissions are required for Config Connector to create and reconcile Kubernetes resources)
