# API Endpoint Overview

<br>

# API Endpoints

| API Endpoint | Description | Purpose |
| --- | --- | --- |
| `/metrics` | An HTTP endpoint that exposes internal performance and resource usage metrics in Prometheus format | Monitoring and observability |
| `/healthz`, `livez`, `readyz` | A simple health check endpoint | Indicates whether a component is alive (200 OK) |
| `/version` | An endpoint that returns the Kubernetes version and build details of the component | For tooling and debugging to confirm compatibility or configuration |
| `/api` | The base endpoint for the core API group | Lists available core resources (*Pods*, *Services*, *ConfigMaps*, *etc.*) |
| `/apis` | The base endpoint for named API groups (*networking.k8s.io*, *apps*, *etc.*) | Lists all available API groups and their versions beyond the core API group |
| `/logs` | Used to fetch logs from a container | Debugging workloads by reading container stdout/stderr |
