# kubectl Overview

```Bash
#
kubectl replace [--force] -f FILENAME.yaml

#
kubectl delete -f FILENAME.yaml
```

<br>

```Bash
#
kubectl scale --replicas=NUMBER -f FILENAME.yaml

#
kubectl scale --replicas=NUMBER replicaset REPLICASET_NAMEcd kn 
```

<br>

```Bash
# Create a deployment
kubectl create -f DEPLOYMENT_DEFINITION.yaml [--namespace=NAMESPACE]

# List deployments
kubectl get deployments

# Update deployment
kubectl apply -f DEPLOYMENT_DEFINITION.yaml

#
kubectl set image RESOURCE_KIND/RESOURCE_NAME CONTAINER_NAME=IMAGE_NAME[:TAG] [FLAGS]

# View deployment rollout statuses
kubectl rollout status deployment/DEPLOYMENT_NAME

# View deployment rollout history
kubectl rollout history deployment/DEPLOYMENT_NAME

#
kubectl expose deployment DEPLOYMENT_NAME --port PORT_NUMBER

# 
kubectl edit deployment DEPLOYMENT_NAME

# 
kubectl scale deployment DEPLOYMENT_NAME --replicas=NUMBER

# Rollback to the previous revision
kubectl rollout undo deployment/DEPLOYMENT_NAME
```

<br>

```Bash
kubectl get pods [--namespace=NAMESPACE] [--selector LABEL=VALUE]
```

<br>

```Bash
# Set a namespace as the current context
kubectl config set-context $(kubectl config current-context) --namespace=NAMESPACE 
```

<br>

```Bash
# Label a node
kubectl label nodes NODE_NAME LABEL=VALUE

# Taint a node
kubectl taint nodes NODE_NAME KEY=VALUE:TAINT_EFFECT
```

<br>

```Bash
# View DaemonSets
kubectl get daemonsets

# Describe a DaemonSet
kubectl describe daemonsets DAEMONSET_NAME
```

<br>

```Bash
#
kubectl get events -o wide
```

<br>

```Bash
# View scheduler logs
kubectl logs SCHEDULER_NAME --name-space=NAMESPACE
```