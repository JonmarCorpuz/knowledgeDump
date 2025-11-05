# Persistent Volume Claim Overview

A **PersistentVolumeClaim** is an object that represents a **request for storage** initiated by a user

* The requested storage will be claimed from a PersistentVolume

![](https://github.com/JonmarCorpuz/publicDiagrams/blob/main/kubernetes-persistent-volume-claim.png)

<br>

# Persistent Volume Claim Access Modes

| Access Mode | Description |
| --- | --- |
| **ReadWriteOnce** | Mounts the PVC as **read-write** by a **single node** |
| **ReadOnlyMany** | Mounts the PVC as **read-only ** by **many nodes** |
| **ReadWriteMany** | Mounts the PVC as **read-write** by **many nodes** |

<br>

# Persistent Volume Claim Deployment

A PersistentVolumeClaim can be defined using a YAML file and then deployed using `kubectl`
```YAML
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: OBJECT_NAME
spec:
  accessModes:
    - ACCESS_MODE 
  resources:
    requests:
      storage: REQUESTED_STORAGE_SIZE
      memory: REQUESTED_MEMORY_SIZE
  storageClassName: standard
```
```Bash
kubectl apply -f FILENAME.yaml
```