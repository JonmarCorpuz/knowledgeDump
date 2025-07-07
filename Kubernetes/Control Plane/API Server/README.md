# API Server Overview

* Acts as the frontend for Kubernetes
* Aware of the static pods created from the kubelet (The static pods will be listed when using kubectl)
* Static pods created by the kubelet will have a read-only mirror object in the kube-apiserver as long as the node is part of the cluster (You can only delete or modify them by modifying the files from the node's manifest folder)