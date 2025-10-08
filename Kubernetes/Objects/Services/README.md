# Kubernetes Services Overview

A service is an API object that provides a stable endpoint to access a set of Pods 

* Enables the communication between various components inside and outside the application
* Helps connect applications together with other applications or users
* Enables loose coupling between microservices in an application

<br>

# Kubernetes Service Types

| Service | Description |
| --- | --- |
| `NodePort` | |
| `ClusterIP` | |
| `LoadBalancer` | |

# NodePort

* Makes an internal pod accessible on a port on the node
* Listens for traffic to a port on the node and forwards that traffic to the pod
* A service will select all the pods that match the defined labels and selectors as endpoints to forward the external requests (It will load balance the load between all the selected pods using the Random algorithm)
* Kubernetes will automatically create a service that spans across all the nodes in the same cluster and map the target port to the same node port on all the nodes in the cluster (Allows users to access the application using the IP of any node in the cluster and the same port number)

<br>

```YAML
apiVersion: v1
kind: Service
metadata:
  # METADATA
spec:
  type: NodePort
  ports:
  - targetPort: # PORT NUMBER of the pod
    port: # PORT NUMBER of the service object
    nodePort: #PORT NUMBER of the node
  selector:
    # LABELS in pod YAML definition from the metadata section
```

<br>

# ClusterIP

* The service creates a virtual IP inside the cluster to enable communication between different services
* Groups multiple pods together to provide a single interface to access them (Helps easily and effectively deploy a microservices0based application on Kubernetes)

<br>

```YAML
apiVersion: v1
kind: Service
metadata:
  # METADATA
spec:
  type: ClusterIP
  ports:
  - targetPort: # PORT NUMBER of the pod
    port: # PORT NUMBER of the service object
  selector:
    # LABELS in pod YAML definition from the metadata section
```

<br>

# LoadBalancer

* Provisions a load balancer for an application
* Only provided in supported cloud providers (If used in a unsupported environment then it'll just be applied as a NodePort)

<br>

```YAML
apiVersion: v1
kind: Service
metadata:
  # METADATA
spec:
  type: LoadBalancer
  ports:
  - targetPort: # PORT NUMBER of the pod
    port: # PORT NUMBER of the service object
    nodePort: #PORT NUMBER of the node
  selector:
    # LABELS in pod YAML definition from the metadata section
```
