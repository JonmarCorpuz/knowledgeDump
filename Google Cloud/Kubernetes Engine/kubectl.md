# kubectl Overview

* You must use a `kubectl` version that's within one minor version difference of your Kubernetes cluster control plane (Ex: *kubectl 1.24 works with 1.23, 1.23, and 1.25 Kubernetes clusters*)

# kubectl Operations

Install kubectl
```Bash
gcloud components install kubectl
```

```Bash
kubectl version --short
```

Display where kubectl is installed
```Bash
which kubectl
```

Change kubectl version
```Bash
cp kubectl kubectl_backup_VERSION
cp kubectl_VERSION kubectl
kubectl version --short
```
