# Namespace Overview

* Doesn't apply to cluster wide resources (*Nodes*, *PVs*, *ClusterRoles*, *ClusterRoleBindings*, *CertificateSigningRequests*, *Namespaces*, *etc.*)

<br>

View namespaces Kubernetes objects
```Bash
kubectl api-resources --namespaced=true
```

<br>

View cluster scoped Kubernetes objects
```Bash
kubectl api-resources --namespaced=false
```