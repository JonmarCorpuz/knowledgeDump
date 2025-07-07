# kubelet Overview

* Relies on the kube-apiserver for instructions on what pods to load on its node (The instructions are decisions made by the Scheduler that was stored in the etcd datastore)
* Can manage a node independently 
* Works at a pod level and can only understand pods (*Create pods*, *Update pods*, *Remove pods*, *etc.*)
* Can be configured to read the pod definition files from a directory on the server designated to store information about pods (The kubelet will then periodically read these files and create pods on the host while ensuring it stays alive and update it should any changes be made)

<br>

# Pod Creation Methods

* The kubelet can create pods from multiple sources at the same time

## Static Local Manifests

<br>

## HTTP API Endpoint

* This is how the kube-apiserver provides input to kubelet