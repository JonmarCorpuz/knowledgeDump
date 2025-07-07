# Static Pods

* Created by the kubelet without intervention from the kube-apiserver
* You can't create replica sets with static pods
* Can be used to deploy the control plane components as pods on a node
* Automatically restarted and updated by the kubelet
* Ignored by the kube-scheduler

<br>

# Static Pods Manifests

* Can be stored in any directory on the node (The location of the directory it's in is passed into the kubelet as an option while running the service)
* Specified in kubelet.service
