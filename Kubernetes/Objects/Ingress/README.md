# Kubernetes Ingress Overview

[Ingress](https://kubernetes.io/docs/concepts/services-networking/ingress/) is an API object that defines the rules for external access to HTTP(S) services in a cluster and implements them via an [Ingress Controller](https://github.com/JonmarCorpuz/knowledgeDump/blob/main/Kubernetes/Objects/Ingress/Ingress%20Controller.md)

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
  - host: example.com
    http:
      paths:
      - path: /testpath1
        pathType: Prefix
        backend:
          service:
            name: test1
            port:
              number: 80
      - path: /testpath2
        pathType: Prefix
        backend:
          service:
            name: test2
            port:
              number: 80
```

<br>

* Think of Ingress as a Layer 7 Load Balancer configured and managed within the cluster
* You still need to expose Ingress to the outside (NodePort, ClusterIP, LoadBalancer)
* You defined rules when you want to route traffic based on different conditions
