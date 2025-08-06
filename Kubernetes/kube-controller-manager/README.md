# kube-controller-manager Overview

The [kube-controller-manager](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-controller-manager/) is a daemon that embeds the core control loops shipped with Kubernetes (*DaemonSet*, *ReplicaSet*, *StatfulSet*, *etc.*)

* A controller is a control loop which is a non-terminating loop that regulates the state of a system 
* Watches the shared state of the cluster through the `kube-apiserver` 
* Makes changes attempting to move the current state towards the desried state

<br>

# Built-in Controllers

| Workload Controller | Description |
| --- | --- |
| Replication Controller |  |
| Deployment Controller |  |
| ReplicaSet Controller |  |
| StatefulSet Controller |  |
| DaemonSet Controller |  |
| Job Controller |  |
| CronJob Controller |  |

<br>

| Node and Resource Controller | Description |
| --- | --- |
| Node Controller |  |
| Endpoints Controller |  |
| ServiceAccount Controller |  |
| Token Controller |  |

<br>

| Namespace and Quota Controller | Description |
| --- | --- |
| Namespace Controller |  |
| ResourceQuota Controller |  |
| LimitRange Controller |  |

<br>

| Garbage Collection Controller | Description |
| --- | --- |
| Garbage Collector |  |