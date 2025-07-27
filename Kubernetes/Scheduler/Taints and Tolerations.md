# Taints and Toleration Overview

A taint is a property that's applied to a node and a toleration is a property that's applied to a pod that tells the tainted node that it can host the pod

* Used to set restrictions on what pods can be scheduled on a node 
* You have a specify which pods can tolerate a tainted node

<br>

# Taints

* Taints are automatically set on the Master node to prevent any pods to be scheduled on this node

## Taint Effect

The taint effect defines what happens to pods that don't tolerate the taint

<br>

| Taint Effect | Description |
| --- | --- |
| NoSchedule | The pod will not be scheduled onto the node at all unless it tolerates the taint |
| PreferNoSchedule | The scheduler will try not to place a pod on the node unless there's no other options |
| NoExecute | Existing pods are evicted within the tolerationSeconds unless they can tolerate the taint |