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
kubectl get pods [--namespace=NAMESPACE]
```

<br>

```Bash
# Set a namespace as the current context
kubectl config set-context $(kubectl config current-context) --namespace=NAMESPACE 
```