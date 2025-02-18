# etcd Overview

`etcd` is the primary distributed key-value store for all cluster state data (*Metadata*, *Configuration data*, *Object status*, *etc.) that's stored and located on the master nodes (The exact location and setup can vary depending on the installation method and the infrastructure it's deployed on)

* Built on the Raft consensus algorithm which help in maintaining consistency across all the nodes in the cluster by ensuring that every change made in one node is replicated to other nodes in the cluster without conflicts
* Designed to handle failures of individual nodes and network partitions while maintaining overall system availability and data correctness (Even if individual nodes withni the etcd cluster fail, the service as a whole remains available and consistent)
* This central storage mechanism allows Kubernetes components to remain stateless
* Helps in synchronizing the state of the cluster across various components and nodes (Whenever a component needs to read or write the state, it interacts with etcd)
* Can be used for service discovery purposes (*Kubernetes stores the IP addresses of pods and services in etcd that can be accessed by other components for routing and load balancing*, *etc.*)

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# etcd Clusters

An `etcd` cluster refers to a group of `etcd` server instances that are stored on the control plane nodes within a Kubernetes cluster and work together to store and replicate that state of a Kubernetes cluster

* Typically run as a cluster of odd-numbered nodes to avoid split-brain scenarios (A condition in distributed computing where clusters become divided due to partial failure or network partition and each subset of the cluster believes that it's the active cluster, which can lead to each subset operating independently of the others)
* Ensure high availability and fault tolerance

