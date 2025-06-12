# Kubernetes Object Overview

A Kubernetes object is a persistent entity in Kubernetes defined within a manifest file 

* Used to represents your cluster's desired state (*What containerized applications are running and on which nodes*, *The resources available to those applications*, *The policies around how those applications behave*, *etc.*)
* Kubernetes will constantly work to ensure that the created object continues to exist via the Kubernetes API (By creating an object, you're telling Kubernetes what its desired state is)

<br>

# Object Configuration

* Almost every K8 object requires the object `spec` and object `status` in order to specify its desired state

## Object Spec

The object spec

<br>

## Object Status

The object status describes the current state of the object

