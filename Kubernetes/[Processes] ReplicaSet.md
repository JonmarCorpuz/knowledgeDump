# Replica Set Overview

A **ReplicaSet** is a controller that's responsible for maintaining a stable set of replica pods running on a node at any given time

* Helps guarantee the availability of a specified number of identical pods
* Automatically creates and deleted pods as needed in order to reach the desired number

![](https://github.com/JonmarCorpuz/publicDiagrams/blob/main/kubernetes-replica-set.png)

<br>

# Replica Set Deployment

A ReplicaSet can be defined using a YAML file and then deployed using `kubectl`
```YAML
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: OBJECT_NAME
spec:
  replicas: REPLICA_NUMBER
  selector:
    matchLabels:
      KEY: VALUE
  template:
    metadata:
      labels:
        KEY: VALUE
    spec:
      containers:
        - name: CONTAINER_NAME
          image: CONTAINER_IMAGE
          ports:
            - containerPort: PORT_NUMBER
```
```Bash
kubectl apply -f FILENAME.yaml
```