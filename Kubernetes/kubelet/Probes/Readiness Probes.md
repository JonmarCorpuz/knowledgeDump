# Readiness Probe Overview

[Readiness Probes](https://kubernetes.io/docs/concepts/configuration/liveness-readiness-startup-probes/#readiness-probe) help the `kubelet` determine whether or not a container is ready to accept traffic

* Useful when waiting for an application to perform time-consuming initial tasks that depend on its backing services (*Network connections*, *Loading files*, *Warming caches*, *etc.*)

<br>

# Readiness Probe Types

## HTTP

```YAML
apiVersion: v1
kind: Pod
metadata:
  name: POD_NAME
spec:
  containers:
  - name: CONTAINER_NAME
    image: CONTAINER_IMAGE
    ports:
    - containerPort: PORT_NUMBER
    readinessProbe:
      httpGet:
        path: ENDPOINT
        port: PORT_NUMBER
      initialDelaySeconds: SECONDS
      periodSeconds: SECONDS
      timeoutSeconds: SECONDS
      failureThreshold: SECONDS
```

<br>

## TCP

Check if a TCP socket is open within a container
```YAML
apiVersion: v1
kind: Pod
metadata:
  name: POD_NAME
spec:
  containers:
  - name: CONTAINER_NAME
    image: CONTAINER_IMAGE[:TAG]
    ports:
    - containerPort: PORT_NUMBER
    readinessProbe:
      tcpSocket:
        port: PORT_NUMBER
      initialDelaySeconds: SECONDS
      periodSeconds: SECONDS
```

<br>

## Exec Command 

Run a command to confirm that the application is ready
```YAML
apiVersion: v1
kind: Pod
metadata:
  name: POD_NAME
spec:
  containers:
  - name: CONTAINER_NAME
    image: CONTAINER_IMAGE[:TAG]
    args: ["COMMANDS"]
    readinessProbe:
      exec:
        command: ["COMMANDS"]
      initialDelaySeconds: SECONDS
      periodSeconds: SECONDS
```