# Kubernetes Ingress Overview

[Ingress](https://kubernetes.io/docs/concepts/services-networking/ingress/) is an API object that manages external access to the services in a user's cluster by exposing HTTP or HTTPS routes from outside the cluster to services within the cluster

* Makes your HTTP network service available using a protocol-aware configuration mechanism that understands web concepts (*URIs*, *Hostnames*, *Paths*, *etc,*)
* May provide load balancing, SSL termination, and name-based virtual hosting
* Doesn't expose arbitrary ports or protocols