# Kubernetes Ingress Overview

[Ingress](https://kubernetes.io/docs/concepts/services-networking/ingress/) is an API object that manages external access to the services in a cluster by exposing HTTP or HTTPS routes from outside the cluster to services within the cluster

* Defines rules to control traffic routing (These rules are implemented with an [Ingress Controller](https://github.com/JonmarCorpuz/knowledgeDump/blob/main/Kubernetes/Objects/Ingress/Ingress%20Controller.md))
* Provides other possible features and configuration options for Services (*externally-reachable URLs*, *Load balance traffic*, *Terminate SSL/TLS*, *etc.*)

<br>
 
```YAML
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: minimal-ingress
  annotations:
    nginx.ingress.kubernetes.io/rewrite-target: /
spec:
  ingressClassName: nginx-example
  rules:
  - http:
      paths:
      - path: /testpath
        pathType: Prefix
        backend:
          service:
            name: test
            port:
              number: 80
```
