# Endpoint Overview

An `Endpoint` is a legacy Kubernetes object that represents the IP addresses and ports of the actual pods that are backing a **Service** (It's how the Service knows where to route traffic)

* Automatically created and managed by Kubernetes when a Service selects one or more pods using label selectors
* Stores information about the pod IPs and the ports on which those pods are listening
* Lists how the Service will find the current pods
* Used other networking components (*kube-proxy*, *DNS*, *etc.*)
* Has **scalability problems** (*Single endpoints object could become very large*, *Updating it causes significant API server and network overhead*, *etc.*)

<br>

| Feature | Endpoint | EndpointSlice |
| --- | --- | --- |
| Scalability | Poor for large Services | High scalability |
| Update Overhead | High (Updates the whole object) | Low (Updates a slice only) |
| Metadata Extensible | Limited | Rich |
| Controller | `kube-controller-manager` | `endpoint-slice-controller` |

<br>

# EndpointSlice 

`EndpointSlices` is a Kubernetes API object that stores a subset of endpoints for a service (Unlike the older Endpoint objects that stores all endpoints in a single object)

* Splits endpoints across multiple resources for better performance (*Low update overhead*, *Supports additional metadata*, *etc.*)
* Designed to work efficiently even with thousands of pods (An extensible replacement for Endpoint objects)gita