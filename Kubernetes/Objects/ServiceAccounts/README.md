# Service Account Overview

* A default service account is automatically created for each namespace within a cluster
* A service account automatically generates a token that's stored as a secrets object that's automatically linked to the service account

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