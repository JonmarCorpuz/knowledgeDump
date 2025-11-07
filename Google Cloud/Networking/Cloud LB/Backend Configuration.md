# Backend Overview

* Defines how traffic is distributed
* Specifies which health check to use
* Indicates if session affinity is used
* Mentions which other services are used (*Cloud CDN*, *IAP*, *etc.*)

<br>

# Backend Types 

## Backend Services

### MIGs

### NEGs

* A configuration object that specifies a group of backend endpoints or services (Commonly used for deploying services in GKE)

| NEG Types | Description |
| --- | --- |
| Zonal | |
| Internet | |
| Serverless | |
| Private Service Connect | |
| Hybrid Connectivity | |

<br>

## Backend Cloud Storage Bucket