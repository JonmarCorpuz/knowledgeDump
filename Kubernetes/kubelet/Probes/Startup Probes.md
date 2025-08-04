# Startup Probe Overview

[Startup probes](https://kubernetes.io/docs/concepts/configuration/liveness-readiness-startup-probes/#startup-probe) verify whether or not an application within a container is started

* Used to adopt liveness checks on slow starting containers in order to avoid having them getting killed by the kubelet before they are up and running

<br>

# Startup Probe Types

## HTTP

Give web applications time to boot
```YAML
apiVersion: v1
kind: Pod
metadata:
  name: startup-http
spec:
  containers:
  - name: myapp
    image: myslowapp:latest
    ports:
    - containerPort: 8080
    startupProbe:
      httpGet:
        path: ENDPOINT
        port: PORT_NUMBER
      failureThreshold: SECONDS
      periodSeconds: SECONDS
    readinessProbe:
      httpGet:
        path: ENDPOINT
        port: PORT_NUMBER
      periodSeconds: SECONDS
```

<br>

## TCP

Give time to a container to open a TCP socket
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
    startupProbe:
      tcpSocket:
        port: PORT_NUMBER
      failureThreshold: SECONDS
      periodSeconds: SECONDS
    livenessProbe:
      tcpSocket:
        port: PORT_NUMBER
      periodSeconds: SECONDS
```

<br>

## Exec Command

```YAM
apiVersion: v1
kind: Pod
metadata:
  name: POD_NAME
spec:
  containers:
  - name: CONTAINER_NAME
    image: CONTAINER_IMAGE
    args: ["COMMANDS"]
    startupProbe:
      exec:
        command: ["COMMANDS"]
      failureThreshold: SECONDS
      periodSeconds: SECONDS
    livenessProbe:
      exec:
        command: ["COMMANDSs
        "]
      periodSeconds: SECONDS
```