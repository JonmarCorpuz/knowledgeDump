# Desired State Overview

The desired state of an object in Kubernetes is the exact configuratio of the object that you define

* K8 uses YAML files as inputs for the creation of K8 objects (*Pods*, *Replicas*, *Deployments*, *Services*, *etc.*)

<br>

# YAML File Properties

```YAML
apiVersion:
kind:
metadata:
spec:
```

## apiVersion

* The version of the Kubernetes API that'll be used to create the object

| Kind | API Version |
| --- | --- |
| Pod | v1 |
| Service | v1 |
| ReplicaSet | apps/v1 |
| Deployment | apps/v1 |

```YAML
apiVersion: # v1, apps/v1
```

<br>

## kind

* The type of object that you're trying to create
* Defined in the form of a dictionary

```YAML
kind: # Pod, Service, ReplicaSet, Deployment, ReplicationController
```

<br>

## metadata

* Data about the object 

```YAML
metadata:
  name: # STRING
  labels:
    # app: STRING 
    # type: STRING
    # env: STRING
  annotations:
```

<br>

## spec

* 

```YAML
spec:
  containers:
    - name: STRING
      image: STRING
```

Pod Template
```YAML
spec:
  template:
    metadata:
      name: # STRING
      labels:
    spec:
      containers:
        - name: # STRING
          image: # STRING
          ports:
            - containerPort: # INTEGER
```

Replication Controller
```YAML
spec:
  replicas: # INTEGER
```

Replica Set
```YAML
spec:
  replicas: # INTEGER
  selector: 
    matchLabels: # STRING
```

<br>