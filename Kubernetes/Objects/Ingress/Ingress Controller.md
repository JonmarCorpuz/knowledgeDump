# Ingress Controller

An Ingress Controller is the implementation of an Ingress that manages the incoming HTTP and HTTPS traffic from outside the cluster and routes it to the appropriate services inside the cluster

* Requires at least one ingress controller running in order for ingress to work
* Not started automatically within a cluster (It needs to be implemented and deployed by the user)
* Responsible for fulfilling the ingress (Usually with a load balancer although it can also configure the user's edge router or additional frontends to help handle the traffic)

<br>

# Ingress Controller Solutions

| Ingress Controller Solution | Description |
| --- | --- |
| tmp | tmp |


<br>

```YAML
apiVersion: apps/v1
kind: Deployment
metadata:
  name: ingress-nginx-controller
  namespace: ingress-nginx
spec:
  replicas: 1
  selector:
    matchLabels:
      app.kubernetes.io/name: ingress-nginx
  template:
    metadata:
      labels:
        app.kubernetes.io/name: ingress-nginx
    spec:
      containers:
      - name: controller
        image: ingress-nginx/controller:latest
        args:
        - /nginx-ingress-controller
        - --configmap=$(POD_NAMESPACE)/ingress-nginx-controller
        ports:
        - containerPort: 80
        - containerPort: 443
```

<br>

Exampl: nginx
* Requires a ConfigMap to feed nginx configuration data
* Requires a ServiceAccount with the right permissions to access the necessary objects
