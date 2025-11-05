# DaemonSet

A DaemonSet is a process that ensures that all the nodes within the same Kubernetes cluster are running a copy of a Pod

![](https://github.com/JonmarCorpuz/publicDiagrams/blob/main/kubernetes-daemon-set.png)

<br>

# DaemonSet Deployment

DaemonSets are defined within a YAML file and deployed using `kubectl`

```YAML
apiVersion: apps/v1
kind: DaemonSet
metadata:
  name: OBJECT_NAME
spec:
  selector:
    matchLabels:
      name: LABEL
  template:
    metadata:
      labels:
        name: DAEMONSET_NAME
    spec:
      containers:
      - name: CONTAINER_NAME
        image: CONTAINER_IMAGE[:TAG]
```
```Bash
kubectl apply -f FILENAME.yaml
```
