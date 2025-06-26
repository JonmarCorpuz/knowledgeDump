# Object State Overview


<br>

# Object States

## Desired States

The desired state is the state you define in your Kubernetes manifests 

<br>

## Current States

The current state is the actual state of Kubernetes objects reported by the control plane

<br>

## Container States

The container state is the operational state of a container within a Pod (`Waiting`, `Running`, `Terminated`)

| Container State | Description |
| --- | --- |
| **Waiting** | The container is not yet running and is waiting to start |
| **Running** | The container is actively running |
| **Terminated** | The container has finished executing either successfully or with failure |

<br>

## Pod States

The Pod state is the current state of a Pod

| Pod State | Description |
| --- | --- |
| **Pending** | Pod was accepted by the API Server but not yet scheduled to a Node |
| **Running** | Pod scheduled to a Node and its containers are running or starting |
| **Succeeded** | All containers in the Pod terminated successfully |
| **Failed** | All containers in the Pod terminated but at least one failed |
| **Unknown** | The state of the Pod can't be determined (The control plane lost contact with the Node) |

<br>

## Node States

The Node state is the current state of a Node 

| Node State | Description |
| --- | --- |
| **Ready** | Node is healthy and can schedule pods |
| **NotReady** | Node is unhealthy or unreachable |
| **Unknown** | The state of the Node can't be determined (The control plane has lost contact with the Node) |
| **MemoryPressure** | Node is running out of memory |
| **DiskPressure** | Node is running out of disk space |
| **PIDPressure** | Node is running out of process IDs |
| **NetworkUnavailable** | Node network is not properly configure |

<br>

