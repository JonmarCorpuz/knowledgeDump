# Kubernetes Network Model Overview

The [Kubernetes network model](https://kubernetes.io/docs/concepts/services-networking/#the-kubernetes-network-model) defines how networking works between objects and external clients in a Kubernetes cluster

* Implemented through CNI plugins (*Calico*, *Cilium*, *etc.*)


<br>

# Network Model Pieces

## Pod Networking

| Pod Networking Requirements | 
| --- | 
| Every pod should have an IP address |
| Every pod should be able to communicate with every other pod in the same node using its given IP address |
| Every pod should be able to communicate with every other pod on the other nodes without NAT |

<br>

Assign unique IP addresses to a node's pods and allow them to communicate with each other on their own node
```Bash
# Create veth pair
ip link add ...

# Attach veth pair
ip link set ...

# Assign IP address
ip -n NAMESPACE addr add ...
ip -n NAMESPACE route add ...

# Bring up the interface
ip -n NAMESPACE link set ...
```

## Node Networking

* Each node will have it's own bridge networking interface that has it's own unique internal IP network

<br>

```Bash
# Add route to the other nodes
ip route add DESTINATION_IP via SOURCE_IP

# Or use a router as the default gateway to manage the routes
```

<br>

## Service API

* Provides a stable and long lived IP address or hostname for a service implemented by one or more backend pods
* Automatically