# Istio Overview

Istio is an open-source service mesh platform that enhances Kubernetes without requiring changes to application code

* Provides advanced traffic management, security, and observability for microservices
* Transparently layers onto existing Kubernetes deployments
* Uses lightweight Envoy proxies as sidecars to intercept and manage all service-to-service communications in the cluster

<br>

# Istio Key Features

| Key Feature | Description |
| --- | --- |
| Traffic Management | |
| Security | |
| Observability | |
| Policy Enforcement | |

<br>

# Istio Components

| Istio Component | Purpose |
| --- | --- |
| istio-ingressgateway | |
| istiod | |
| istio-egressgateway | |

<br>

# Installing Istio

## Istioctl

```Bash
istioctl install --set profile=PROFILE -y

istioctl verify-install
```

| Istioctl Profile | Description |
| --- | --- |
| demo | |

<br>

## Istio Operator

<br>

## Helm
