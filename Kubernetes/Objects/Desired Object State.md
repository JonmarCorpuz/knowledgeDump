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
kind: # Pod, Service, ReplicaSet, Deployment, ReplicationController, Namespace, ResourceQuota
```

<br>

| Kind | Description |
| --- | --- |
| Pod | |
| Service | |
| ReplicaSet | |
| ReplicationController | |
| Deployment | |
| Namespace | |
| ResourceQuota | |
| ServiceAccount | |

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

Toleration
```YAML
apiVersion:
kind: Pod
metadata:
  name: POD_NAME
spec
  containers:
  - name: CONTAINER_NAME
    image: CONTAINER_IMAGE
  
  tolerations:
  - key = "KEY"
    operation = "Equal"
    value = "VALUE"
    effect = "TAINT_EFFECT"
```

Node Selectors
```YAML
apiVersion:
kind: Pod
metadata:
  name: POD_NAME
spec:
  containrers:
  - name: CONTAINER_NAME
    image: CONTAINER_IMAGE

  nodeSelector:
    LABEL: VALUE 
```

Node Affinity
```YAML
apiVersion:
kind: Pod
metadata:
  name: POD_NAME
spec:
  containrers:
  - name: CONTAINER_NAME
    image: CONTAINER_IMAGE

  affinity:
    nodeAffinity:
      requiredDuringSchedulingIgnoreDuringExecution:
        nodeSelectorTerms:
        - matchExpressions:
          - key: LABEL
            operator: OPERATOR # In, NotIn, Exists, DoesNotExist
            values:
            - VALUE
              VALUE
```

Limit Ranges
```YAML
apiVersion: v1
kind: LimitRange
metadata:
  name: OBJECT_NAME
spec:
  limits:
    # Default limit
  - default:
      cpu: 500m
      memory: 1Gi
    # Default request
    defaultRequest:
      cpu: 500m
      memory: 1Gi      
    # Maximum limit that can be set 
    max:
      cpu: "1"
      memory: 1Gi
    # Minimum limit that can be set
    min:
      cpu: 100m
      memory: 1Gi
    type: container
```

Resource Quotas
```YAML
apiVersion: v1
kind: ResourceQuota
metadata:
  name: RESOURCE_NAME
spec:
  hard:
    requests.cpu: 4
    requests.memory: 4Gi
    limits.cpu: 10
    limits.memory: 10Gi
```

DaemonSet
```YAML
apiVersion: apps/v1
kind: DaemonSet
metadata:
  name: RESOURCE_NAME
spec:
  selector:
    matchLabels:
      LABEL: VALUE
  
  template:
    metadata:
      labels:
        LABEL: VALUE
      spec:
        containers:
        - name: CONTAINER_NAME
          image: CONTAINER_IMAGE
```

Schedulers
```YAML
apiVersion: kubescheduler.conf.k8s.io/v1
kind: LubeSchedulerConfiguration
profiles:
- schedulerName: SCHEDULER_NAME
```
```YAML
apiVersion: v1
kind: Pod
metadata:
  name: RESOURCE_NAME
  namespace: NAMESPACE
spec:
  containers:
  - command:
    - kuber-scheduler
    - --address=127.0.0.1
    - --kubeconfig=/etc/kubernetes/scheduler.conf
    - --config=/etc/kubernetes/SCHEDULER_CONFIGURATION.yaml

    image: k8s.gcr.io/kube-scheduler-amd64:v1.11.3
    name: kube-scheduler
```

Deploy Pod Using Custom Scheduler
```YAML
apiVersion: v1
kind: Pod
metadata:
  name: RESOURCE_NAME
spec:
  containers:
  - image: CONTAINER_IMAGE
    name: CONTAINER_NAME

  schedulerName: SCHEDULER_NAME
```

<br>
