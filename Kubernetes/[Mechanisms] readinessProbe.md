# Readiness Probe Overview

A **readinessProbe** is a mechanism used to check whether a container inside a pod is **ready to handle requests**

* Ensures that a container is excluded from the service endoints until it's actually ready to serve traffic

![](https://github.com/JonmarCorpuz/publicDiagrams/blob/main/kubernetes-readiness-probe.png)

<br>

# Readiness Probe Types

## HTTP Readiness Probe

An **HTTP** readiness probe makes an **HTTP GET** request to the specified endpoint of the container

* The container is marked as ready if it returns a 2xx or 3xx response

<br>

An HTTP readiness probe is defined in the `spec` section of a pod's YAML definition file and deployed using `kubectl`
```YAML
spec:
  containers:
  - name: CONTAINER_NAME
    image: CONTAINER_IMAGE[:TAG]
    readinessProbe:
      httpGet:
        path: ENDPOINT
        port: PORT_NUMBER
      initialDelaySeconds: SECONDS
      periodSeconds: SECONDS
```
```Bash
kubectl apply -f FILENAME.yaml
```

<br>

## TCP Socket Readiness Probe

A **TCP socket** readiness probe tries to open a **TCP connection** on the specified port of the container

* The container is marked as ready if the connection succeeds

<br>

A TCP socket readiness probe is defined in the `spec` section of a pod's YAML definition file and deployed using `kubectl`
```YAML
spec:
  containers:
  - name: CONTAINER_NAME
    image: CONTAINER_IMAGE[:TAG]
    readinessProbe:
      tcpSocket:
        port: PORT_NUMBER
      initialDelaySeconds: SECONDS
      periodSeconds: SECONDS
```
```Bash
kubectl apply -f FILENAME.yaml
```

<br>

## Exec Readiness Probe

An **exec** readiness probe tries to run a command inside the container

* The container is marked as ready if the command exits with a code **0**

<br>

An exec readiness probe is defined in the `spec` section of a pod's YAML definition file and deployed using `kubectl`
```YAML
spec:
  containers:
  - name: CONTAINER_NAME
    image: CONTAINER_IMAGE[:TAG]
    readinessProbe:
      exec:
        command:
          - COMMAND
      initialDelaySeconds: SECONDS
      periodSeconds: SECONDS
```
```Bash
kubectl apply -f FILENAME.yaml
```