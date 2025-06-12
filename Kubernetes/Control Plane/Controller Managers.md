# Controller Manager Overview

A controller manager is a daemon that comes with Kubernetes and embeds the core control loops (Controllers) 

<br>

# Controller Manager Components

## Controllers

A controller is a control loop that watches the shared state of the cluster through the apiserver

* Responsible for making the current state of an object come closer to the desried state
* A single controller always tracks at least one Kubernetes resource type (These objects have a spec field that represents the desired state)
* Manages the state of objects by interacting with the cluster API server
* Updates the objects that configure the controllers (Ex: *The Job controller will update a Job object to mark it Finished once the work is done for that Job*)

<br>

## Job Controller

* When the Job controller sees a new task it makes sure that the kubelets on a set of Nodes are running the right number of Pods to get the work done
* Doesn't run any Pods or containers itself rather it tells the API server to create or remove Pods (The other components in the control plane will act on the new information)

<br>

## Replication Controller

<br>

## Endpoints Controller

<br>

## Namespace Controller

<br>

## Serviceaccounts Controller
