# DaemonSet Overview

* Automatically a copy of a pod on each node in a cluster to ensure that one copy of the pod is always present in all worker nodes (Both on already existing and new nodes)
* Useful to deploy various workloads (*kube-proxy*, *monitoring agents*, *log viewers*, *networking solutions*, *etc.*)
* Uses NodeAffinity and the default scheduler to schedule pods on nodes
* Ignored by the kube-scheduler