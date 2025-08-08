# Weave CNI Overview

<br>

Deploy Weave
```Bash
kubectl apply -f "https://cloud.weave.works/k8s/net?k8s-version=$(kubectl version | base64 | tr -d '\n')"
```

<br>

View Weave peers
```Bash
kubectl get pods -n kube-system
```