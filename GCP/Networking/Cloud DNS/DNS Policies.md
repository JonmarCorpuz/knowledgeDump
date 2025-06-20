# Cloud DNS Policy Overview

* Provide a flexible way to refine how an organization uses DNS

<br>

# Cloud DNS Policy Types

## Server Policies

* Applies private DNS configuration to a VPC network
* Used to set up hybrid deployments for DNS resolution
* Each VPC network can have a DNS policy (An inbound server policy can be set up depending on the direction of the DNS resolutions and an outbound server policy can be used to set up DNS forwarding for workloads that use an on-premises DNS resolver)
* On-premise workloads require an inbound server policy in order to resolve Cloud DNS Private zones

<br>

## Response Policies

A Cloud DNS private zone concept that contains rules instead of records

* Enables users to modify the behavior of the DNS resolver by using rules that they define
* Lets users introduce customized rules in DNS servers within their network that the DNS resolver consults during lookups
* Managed separately in the API (These are not DNS zones)

<br>

## Routing Policies

* Used to steer traffic based on specific criteria (Routing policies)
* Only one type of routing policy can be applied to a resoure record set at a time
* Nesting and combining routing policies is not supported

### Weighted Round Robin Routing POlicy

### Geolocation Routing Policy

### Failover Routing Policy

* For private zones only