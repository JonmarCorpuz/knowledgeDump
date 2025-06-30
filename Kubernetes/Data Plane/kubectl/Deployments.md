# kubectl Deployment Commands

Create a deployment
```Bash
kubectl create -f DEPLYMENT.yaml
```

<br>

Update deployment (Deploy new rollout)
```Bash
kubectl apply -f DEPLOYMENT.yaml
```

<br>

List deployments
```Bash
kubectl get deployments
```

<br>

Rollback
```Bash
kubectl rollout undo deployment/DEPLOYMENT.yaml
```

<br>

View rollout status
```Bash
kubectl rollout status deployment/DEPLOYMENT-NAME
```

<br>

```Bash
kubectl rollout history deployment/DEPLOYMENT-NAME
```

<br>

```Bash
kubectl get replicasets
``` 