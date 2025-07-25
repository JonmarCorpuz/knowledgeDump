# Admission Controller Overview

An **admission controller** is a software component (plugin) within the Kubernetes API server that checks the data arriving in a request to modify a resource

* Interceps requests to the Kubernetes API server after authentication and authorization (Before the object is persisted in etcd)
* Part of the control plane logic that decides whether a request should be allowed, denied, or modified
* Validates an API request (Rejects it if a policy is violated)
* Mutates an API object (*Inject labels*, *Inject sidecars*, *etc.*)
* Denies a request that doesn't meet certain rules or policies 
* Works with admission webhooks

<br>

# Admission Control Phases

## Mutating Admission Controllers

A **mutating admission controller** modified the request object before validation (*Adds a label*, *Modifies the spec*, *etc.*)

<br>

## Validating Admission Controllers

A **validation admission controller** only validates the request after all mutations

<br>

# Admission Plugins

An admission plugin is a specific implementation (code module) of an admission controller

<br>

Enable admission plugins
```Bash
kube-apiserver --enable-admission-plugins=ADMISSION_PLUGINS
```

<br>

| Webhook Admission Plugin | Description |
| --- | --- |
| `MutatingAdmissionWebhook` (For custom policies) | Calls external webhooks to modify requests (*Add sidecars*, *etc.*) |
| `ValidatingAdmissionWebhook` (For custom policies) | Calls external webhooks to validate requests (*Enforce custom policies*, *etc.*) |
| `ImagePolicyWebhook` | Calls an external webhook to validate images before pod creation |

<br>

| Resource Management Admission Plugin | Description |
| --- | --- |
| `LimitRanger` | Enforces default limits and quotas on resource usage in namespaces |
| `ResourceQuota` | Enforces quota limits on resource usage per namespace |
| `DefaultTolerationSeconds` | Adds default tolerations to pods to avoid indefinite scheduling |

<br>

| Security and Policy Enforcement Admission Plugin | Description |
| --- | --- |
| `PodSecurity` | Enforces PSS |
| `NodeRestriction` | Restricts what kubenets (nodes) can modify |
| `DenyServiceExternalIPs` | Blocks setting external IPs for Services unless explicitly allowed |
| `AlwaysPullImages` | Forces the image pull policy to **Always** in order to ensure fresh image pulls |

<br>

| Defaults Admission Plugin | Description |
| --- | --- |
| `ServiceAccount` | Automatically assigns service accounts and mounts tokens into pods |
| `DefaultStorageClass` | Automatically assigns a default StorageClass to PVCs that don't specify one |
| `DefaultIngressClass` | Sets the default IngressClass for Ingresses that do specify one |

<br>

| Admission Plugin | Description |
| --- | --- |
| `NamespaceLifecycle` | Ensures resources are not created in non-existent or terminating namespaces |
| `RuntimeClass` | Applies RuntimeClass to pods for different container runtimes |
| `PersistentVolumeLabel` (Deprecated) | Automatically adds zone labels to PVs |
| `TaintNodesByCondition` | Adds taints to nodes based on their conditions (Used with scheduler) |
| `Priority` | Applies pod priority and preemption logic |
| `ExtendedResourceToleration` | Automatically tolerates extended resources (*GPU*, *etc.*) |
| `PodTolerationRestriction` | Restricts what tolerations pods can have |
| `EventRateLimit` | Limits the rate of event creation to prevent API server overload |

<br>

# Admission Webhooks

An **admission webhook**

<br>

# Admission Webhooks

## Mutating Webhooks

A mutating admission webhook intercepts API requests after authentication and authorization to add, remove, or modify fields in the incoming object 

* Adds, removes, or modifies fields in the incoming Kubernetes object
* Automatically injects configurations (*Labels*, *Sidecar containers*, *Annotations*, *etc.*)

<br>

##