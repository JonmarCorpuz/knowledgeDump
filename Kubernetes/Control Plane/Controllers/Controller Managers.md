# Controller Manager Overview

A controller manager is a daemon that comes with Kubernetes and embeds the core control loops (Controllers) 

<br>

# Controller Manager Components

## Controllers

A controller is a **control loop that watches the shared state of the cluster** through the apiserver

* Responsible for making the current state of an object come closer to the desried state
* A single controller always tracks at least one Kubernetes resource type (These objects have a spec field that represents the desired state)
* Manages the state of objects by interacting with the cluster API server
* Updates the objects that configure the controllers (Ex: *The Job controller will update a Job object to mark it Finished once the work is done for that Job*)

<br>

## Job Controller

* When the Job controller sees a new task it makes sure that the kubelets on a set of Nodes are running the right number of Pods to get the work done
* Doesn't run any pods or containers itself rather it tells the API server to create or remove Pods (The other components in the control plane will act on the new information)

<br>

## Replication Controller

<br>

## Endpoints Controller

<br>

## Namespace Controller

<br>

## Serviceaccounts Controller

<br>

## Cloud Controller Manager

The [cloud-controller-manager](https://kubernetes.io/docs/concepts/architecture/cloud-controller/) lets users link their acluster into their specific cloud provider's API

* Separates out the components that interact with that cloud platform from components that only interact with their cluster
* Runs in the control plane as a replicated set of processes

<br>

## Node Controller

The [node controller](https://kubernetes.io/docs/concepts/architecture/nodes/#node-controller) is responsible for updating node objects and other various aspects of Nodes

* Assigns a CIDR block to the node when it's registered (If CIDR assignment is turned on)
* Keeps the node controller's internal list of nodes up to date with the cloud provider's list of available machines (When running in a cloud environment and whenever a node is unhealthy, it'll ask the cloud provider if the VM for that node is still available and if not, the node controller deletes it from its list of nodes)
* Updates the Ready condition in the node's .status field to Unknown if the node becomes unreachable (If the node remains unreachable, it'll trigger [API-initiated eviction](https://kubernetes.io/docs/concepts/scheduling-eviction/api-eviction/) for all the pods on that node)
* Checks the state of each node every 5 seconds by default
* Doesn't evict pods from more than 1 node per 10 seconds by default but can change when a node in a given availability zone becomes unhealthy

<br>

## Route Controller
