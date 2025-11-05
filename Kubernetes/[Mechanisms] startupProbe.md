
# Startup Probe Overview

A **startupProbe** is a mechanism used to check whether a container inside a pod has **started up successfully**

<br>

# Startup Probe Types

## HTTP Startup Probe

<br>

```YAML
spec:
  template:
    metadata:
      labels:
        KEY: VALUE
    spec:
      containers:
      - name: CONTAINER_NAME
        image: CONTAINER_IMAGE[:TAG]
        startupProbe:
          httpGet:
            path: ENDPOINT
            port: PORT_NUMBER
          failureThreshold: SECONDS
          periodSeconds: SECONDS
```
```Bash
kubectl apply -f FILENAME.yaml
```

<br>

## TCP Socket Startup Probe

<br>

```YAML
spec:
  template:
    metadata:
      labels:
        KEY: VALUE
    spec:
      containers:
      - name: CONTAINER_NAME
        image: CONTAINER_IMAGE[:TAG]
        startupProbe:
          tcpSocket:
            port: PORT_NUMBER
          failureThreshold: SECONDS
          periodSeconds: SECONDS
```
```Bash
kubectl apply -f FILENAME.yaml
```

<br>

## Exec Startup Probe

<br>

```YAML
spec:
  containers:
  - name: CONTAINER_NAME
    image: CONTAINER_IMAGE
    args:
    - COMMAND
    startupProbe:
      exec:
        command:
        - COMMAND
      initialDelaySeconds: SECONDS
      periodSeconds: SECONDS
      failureThreshold: SECONDS
```
```Bash
kubectl apply -f FILENAME.yaml
```