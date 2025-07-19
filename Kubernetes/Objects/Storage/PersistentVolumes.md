# Persistent Volume Overview

A persistent volume is a Kubernetes object that represents real storage and lives independently of pods 

* Either manually provisioned or dynamically created using a storage class

<br>

# Persistent Volume Definition

```YAML
apiVersion: v1
kind: PersistentVolume
metadata:
  name: PERSISTENT_VOLUME_NAME
spec:
  capacity:
    storage: TOTAL_STORAGE
  accessModes:
    - ACCESS_MODE
  persistentVolumeReclaimPolicy: RECLAIM_POLICY
  hostPath:
    path: MOUNT_PATH
```

<br>

| Persistent Volume Concept | Description | Possible Values |
| --- | --- | --- |
| `capacity` | Specifies the total storage size the the volume provides | `storage: TOTAL_STORAGE` |
| `accessModes` | Defines how the PV can be accessed | `ReadWriteOnce` (Read-write by a single node), `ReadOnlyMany` (Read-only by many nodes), `ReadWriteMany` (Read-write by many nodes although requires a supported volume plugin) |
| `persistentVolumeReclaimPolicy` | Defines what happens to the PV and its data after the associated PVC is deleted | `Retain` (Keeps the data on the volume after the PVC is released but requires manual cleanup), `Delete` (Deletes the storage resource after the PVC is released), `Recycle` (Clears the contents and makes the PV available again) |
| `hostPath` | Specifies where the PV maps to on the node's filesystem | `path: MOUNT_PATH` |

<br>

# Persistent Volume Claims

A persistent volume claim is a request for storage made by a user or application (It's how pods ask for persistent storage without needing to know the details of the physical volume)

* Claims a PV that matches the requested size, access mode, and storage class
* Doesn't require the developer to know the underlying storage details

<br>

Create PVC
```YAML
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: PVC_NAME
spec:
  accessModes:
    - ACCESS_MODE
  resources:
    requests:
      storage: TOTAL_STORAGE
# storageClassName: STORAGE_CLASS
```

<br>

User a PVC in a pod
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
          name: VOLUME_MOUNT_NAME
  volumes:
    - name: VOLUME_NAME
      persistentVolumeClaim:
        claimName: PVC_NAME
```