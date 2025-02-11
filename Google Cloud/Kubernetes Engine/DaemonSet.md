# DaemonSet Overview

A DaemonSet is a type of workload controller used to manage the deployment of certain types of Pods across a cluster

* Primarily ensures that all or a subset of Kubernetes nodes run a copy of a specific Pod (If there are a certain number of Nodes in the cluster, and the DaemonSet specifies a certain Pod, then that Pod will be running on all Nodes)
* As new Nodes are added to the cluster, Kubernetes automatically adds a copy of the specified Pod to the Nodes according to the DaemonSet specification (Similarly, if a Node is removed from the cluster, the Pods running as part of the DaemonSet on that Node are also removed)
* Guarantees that every Node in the cluster runs a copy of a specified Pod

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# DaemonSet Configuration

```YAML
apiVersion: apps/v1
kind: DaemonSet
```
