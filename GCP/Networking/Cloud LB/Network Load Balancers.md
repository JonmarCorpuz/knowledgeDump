# Network Load Balancer Overview

* Works on the ntranport layer (Layer 4)
* Handles TCP, UDP, and other IP protocol traffic

<br>

# Network Load Balancer Types

| Network Load Balancer Type | Description |
| --- | --- |
| Proxy | |
| Passthrough | |

## Proxy 

| Proxy Network Load Balancer Type | Description |
| --- | --- |
| External | |
| Internal | |

* Directly forwards traffic to the backend while preserving the original source IP address

### External

#### Global

#### Regional

<br> 

### Internal

* Can be used as the next hop (Load balancer and route must be in the same VPC)
* Can be used to load balance to multiple NICs (VMs must have ip forwarding enabled)

#### Regional

#### Cross-Region

<br>

## Passthrough

| Passthrough Network Load Balancer Type | Description |
| --- | --- |
| External | |
| Internal | |

### External 

<br>

#### Regional

### Internal

#### Regional