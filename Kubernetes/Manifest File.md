# Manifest File Overview

A Kubernetes manifest file is a YAML or JSON file that describes how an application or service should be deployed and managed on the Kubernetes platform

* Contains the necessary specifications for Kubernetes resources (*Pods*, *Services*, *Deployments*, *etc.*)

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Manifest File Components

## API Version

The `API version` section specifies the version of the Kubernetes API you're using to create the object

```YAML
apiVersion: API_VERSION
```

## Kind

The `kind` section specifies the type of resource you want to create

```YAML
kind: RESOURCE_TYPE
```

| Resource Type | Description |
| --- | --- |
| Pod | |
| Service | |
| Deployment | |
| StatefulSet | |
| DaemonSet | |

## Metadata

The `metadata` includes data that uniquely identifies the resource within a namespace

```YAML

```

| Metadata Type | Description |
| --- | --- |
| name | The name of the resource |
| namespace | The namespace in which the resource will be created (Optional if default is used) |
| label | A key-value pair that's used to organize, select, and categorize resources |
| annotations | Non-identifying metadata which can be used to store additional information helpful to clients |

## Specification

The `spec` section defines the desired state of the resource

```YAML

```

| Specification Type | Description |
| --- | --- |
| replicas | The number of instances for the resource |
| selector | The criteria that identifies the set of pods/objects the resource applies to |
| template | The template used for creating the pods for deployments |

### Container Specification 

| Container Specification Element | Description |
| --- | --- |
| name | The name of the container within the pod |
| image | The Docker image to use for the container |
| ports | The list of ports to expose from the container |
| env | The environment variables to set in the container |
| resource requests | The amount of resources (*CPU*, *Memory*) that Kubernetes will guarantee to the container |
| resource limits | The maximum amount of resources (*CPU*, *Memory*) that the container can use |
| volumeMounts name | A reference to the volume name |
| volumeMounts mountPath | The path within the container at which the volume should be mounted |
| volumes name | The name of the volume reference in the volumeMounts |
| volumes emptyDir | Specifies that the volume is a temporary directory that shares the pod's lifetime |
| volumes configMap | |
| volumes persistentVolumeClaim | |
| volumes secret | |

```YAML
# Container specification template
spec:
  containers:
    - name: CONTAINER_NAME
      image: IMAGE:TAG
      ports"
        - containerPort: PORT_NUMBER
      env:
        - name: MY_ENV_VAR
          value: "VALUE"
      resources:
        requests:
          memory: "MEMORY"
          cpu: "CPU"
        limits:
          memory: "MEMORY"
          cpu: "CPU"
      volumeMounts:
        - name: VOLUME_NAME
          mountPath: MOUNT_PATH
  volumes:
    - name: VOLUME_NAME
      emptyDir: {}
```
