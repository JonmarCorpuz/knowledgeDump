# Service Mesh Overview

A service mesh is a dedicated and configurable infrastructure layer that handles the communication between services without having to change the code in a microservice architecture

* Separates service-to-service networking logic from application code
* Uses sidecar proxies to take care of all the tasks that should be outsourced from the microservice (The sidecar proxies and the communication between them form the data plane)

<br>

# Service Mesh Components

## Data Plane

* Each microservice container is paired with a lightweight proxy that intercepts all network traffic to and from the service
* The sidecar proxies to take care of all the tasks that should be outsourced from the microservice
* The sidecar proxies and the communication between them form the data plane

<br>

| Data Plane Component | Purpose |
| --- | --- |
| Sidercar Proxy | |
| Istio Agent | |

## Control Plane 

* Configures and coordinates all sidecar proxies in order to enforce global policies, distribute routing rules, maintain a registry of services, and collect telemetry data for monitoring and troubleshooting

<br>

| Control Plane Component | Purpose |
| --- | --- |
| `Istiod` | |

<br>

# Service Mesh Benefits

| Service Mesh Benefit | Description |
| --- | --- |
| Traffic Management | |
| Observability | |
| Security | |
| Resilience | |
