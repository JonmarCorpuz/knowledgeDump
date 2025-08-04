# Liveness Probe Overview

[Liveness probes](https://kubernetes.io/docs/concepts/configuration/liveness-readiness-startup-probes/#liveness-probe) help determine if a container is still running and responsive (*The kubelet restarts the container if it fails its liveness probe repeatedly*, *etc.*)

* Liveness probes don't wait for readiness probes to success (Use either `initialDelaySeconds` or a startup probe to instruct the kubelet to wait before executing a liveness probe)

<br>

# Liveness Probe Types

## HTTP 

Check the health of an HTTP endpoint inside a container
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
    livenessProbe:
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

Check if a TCP socket is open inside a container
```YAML
apiVersion: v1
kind: Pod
metadata:
  name: POD_NAME
spec:
  containers:
  - name: CONTAINER_NAME
    image: CONTAINTER:IMAGE[:TAG]
    ports:
    - containerPort: PORT_NUMBER
    livenessProbe:
      tcpSocket:
        port: PORT_NUMBER
      initialDelaySeconds: SECONDS
      periodSeconds: SECONDS
```

<br>

## Exec Command

Run a command inside within a container (Container is healthy if the command exits successfully)
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
    livenessProbe:
      exec:
        command: ["COMMANDS"]
      initialDelaySeconds: SECONDS
      periodSeconds: SECONDS
```