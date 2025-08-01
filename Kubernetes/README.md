# Kubernetes Overview

* A container orchestration tool to automate the deployment and management of multiple containers in a cluster environment
* Uses YAML files to represent configuration data

<br>

| Master Node Port | Service |
| --- | --- |
| 2379 | etcd server |
| 2380 | etcd client |
| 6443 | kube-apiserver |
| 10250 | kubelet |
| 10257 | kube-controller-manager |
| 10259 | kube-scheduler |

<br>

| Worker Node Port | Description |
| --- | --- |
| 10250 | kube-apiserver |
| 3000 - 32767 | NodePort services |