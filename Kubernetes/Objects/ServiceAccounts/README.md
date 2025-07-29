# Service Account Overview

* A service account named default is automatically created for each namespace within a cluster (This default service account and its token are automatically mounted to that pod as a volume mount )
* A service account automatically generates a token that's stored as a secrets object that's automatically linked to the service account
* Can't be modified when being used by a Kubernetes resource

<br>

List all service accounts
```Bash
kubectl get serviceaccount
```

<br>

List more details for a service account
```Bash
kubectl describe serviceaccount SERVICE_ACCOUNT_NAME
```

<br>

View a service account's secret token
```Bash
kubectl describe secret SECRET_NAME
```