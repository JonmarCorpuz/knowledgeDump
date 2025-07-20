# Pod Overview

A pod is a group of one or more containers

* The smallest object that can be created in Kubernetes
* A single instance of an application
* Usually have a one-to-one relationship with containers but a single pod can have multiple containers except for the fact that there's usually not multiple containers of the same kind (*Helper container doing some support task for the application and that lives along side a container by maintaining a one-to-one relationship with their respective container*, *etc.*)
* Containers within the same Pod can communicate with each other as local hosts since they share the same space (They can also share the same storage space)

<br>

```YAML
apiVersion: v1
kind: Pod
metadata:
  name: POD_NAME
spec:
  containers:
    - name: CONTAINER_NAME
      image: CONTAINER_IMAGE
      volumeMounts:
        - mountPath: MOUNT_PATH
          name: VOLUME_NAME
  volumes:
    - name: VOLUME_NAME
      persistentVolumeClaim:
        claimName: EXISTING_PVC_NAME
```

<br>

| Pod Container Concept | Description | Possible Options |
| --- | --- | --- |
| `name` | The name of the container | |
| `image` | The container image to use | |
| `volumeMounts` | | `mountPath: MOUNT_PATH` (The path inside the container where the volume will be mounted), `name` (Refers to the volume name) |

<br>

| Pod Volume Concept | Description | Possible Options |
| --- | --- | --- |
| `name` | The name used to link the volume to volumeMounts | |
| `persistentVolumeClaim` | Indicates the volume is backed by a PVC | `claimName: EXISTING_PVC_NAME` (Kubernetes will bind this pod to the PV associated with this PVC) |

<br>

# Static Pods

* Created by the kubelet without intervention from the kube-apiserver
* You can't create replica sets with static pods
* Can be used to deploy the control plane components as pods on a node
* Automatically restarted and updated by the kubelet
* Ignored by the kube-scheduler

<br>

## Static Pods Manifests

* Can be stored in any directory on the node (The location of the directory it's in is passed into the kubelet as an option while running the service)
* Specified in kubelet.service
