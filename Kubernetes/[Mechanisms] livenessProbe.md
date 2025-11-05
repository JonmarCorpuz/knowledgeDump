# Liveness Probe Overview

A liveness probe is a mechanism used to check whether a container inside a pod is still running and healthy

* If it fails repeatedly then kubernetes will kill the container and follow the pod's restart policy to bring it back up

![](https://github.com/JonmarCorpuz/publicDiagrams/blob/main/kubernetes-liveness-probe.png)

<br>

# Liveness Probe Types

## HTTP Liveness Probe

An HTTP liveness probe makes an **HTTP GET** request to the specified endpoint on the container 

* The container is marked as healthy if it returns a 2xx or 3xx response

An HTTP liveness probe is defined in the `spec` section of a pod's YAML definition file and deployed using `kubectl`

```YAML
spec:
  containers:
  - name: CONTAINER_NAME
    image: CONTAINER_IMAGE[:TAG]
    livenessProbe:
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

## TCP Socket Liveness Probe

A TCP socket liveness probe tries to open a TCP connection on the specified port

* The container is marked as healthy if the connection succeeds

An HTTP liveness probe is defined in the `spec` section of a pod's YAML definition file and deployed using `kubectl`

```YAML
spec:
  containers:
  - name: CONTAINER_NAME
    image: CONTAINER_IMAGE[:TAG]
    livenessProbe:
      tcpSocket:
        port: PORT_NUMBER
      initialDelaySeconds: SECONDS
      periodSeconds: SECONDS
```
```Bash
kubectl apply -f FILENAME.yaml
```

<br>

## Exec Liveness Probe

An exec liveness probe tries to run a command inside the container 

* The container is marked as healthy if the command exits with a code **0**

```YAML
spec:
  containers:
  - name: CONTAINER_NAME
    image: CONTAINER_IMAGE[:TAG]
    livenessProbe:
      exec:
        command:
        - COMMAND
      initialDelaySeconds: SECONDS
      periodSeconds: SECONDS
```
```Bash
kubectl apply -f FILENAME.yaml
```
