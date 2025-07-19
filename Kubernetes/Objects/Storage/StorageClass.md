# Storage Class Overview

A `StorageClass` is an object that defines how persistent volumes should be provisioned

* Enables automatic and dynamic PV creation with specific storage backend configurations when a PVC is created (Users would need to manually create PVs and match them to PVCs without a storage class)

<br>

# Storage Class Definition

```YAML
apiVersion: storage.k8s.io/v1
kind: StorageClass
metadata:
  name: STORAGE_CLASS_NAME
  annotations:
    storageclass.kubernetes.io/is-default-class: "false"
provisioner: CSI_DRIVER # The CSI driver that's responsible for provisioning volumes
reclaimPolicy: RECLAIM_POLICY 
allowVolumeExpansion: true
mountOptions:
  - discard # this might enable UNMAP / TRIM at the block storage layer
volumeBindingMode: WaitForFirstConsumer
parameters:
  guaranteedReadWriteLatency: "true" # provider-specific
```

<br>

| Storage Class Concept | Description | Value Options |
| --- | --- | --- |
| `provisioner` | The plugin that provisions the volume on the underlying storage system | |
| `reclaimPolicy` | What happens to the volume after the PVC is deleted | `Delete` or `Retain` |
| `volumeBindingMode` | When the PV gets created | `WaitForFirstConsumer` |
