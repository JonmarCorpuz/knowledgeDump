# Admission Webhook Overview

<br>

# Admission Controller

An **admission controller** is a software component (plugin) within the Kubernetes API server that checks the data arriving in a request to modify a resource

* Interceps requests to the Kubernetes API server after authentication and authorization (Before the object is persisted in etcd)
* Part of the control plane logic that decides whether a request should be allowed, denied, or modified
* Validates an API request (Rejects it if a policy is violated)
* Mutates an API object (*Inject labels*, *Inject sidecars*, *etc.*)
* Denies a request that doesn't meet certain rules or policies 
* Works with admission webhooks

## Mutating Admission Controllers

A **mutating admission controller** modified the request object before validation (*Adds a label*, *Modifies the spec*, *etc.*)

<br>

## Validating Admission Controllers

A **validation admission controller** only validates the request after all mutations

<br>

# Admission Requests

An **admission request** is an object sent to an admission controller

<br>

# Admission Webhooks

## Mutating Webhooks

A mutating admission webhook intercepts API requests after authentication and authorization to add, remove, or modify fields in the incoming object 

* Adds, removes, or modifies fields in the incoming Kubernetes object
* Automatically injects configurations (*Labels*, *Sidecar containers*, *Annotations*, *etc.*)

<br>

##