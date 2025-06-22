# Private Connection Methods

* Uses interal IP addresses
* Proivdes quicker and more secure access to Google resources
* Supported by all GCP APIs and services
* Traffic stays on the Google backbone network

<br>

# Private Access Options

| Private Google Access | Private Service Connect | Private Service Access |
| --- | --- | --- |
| Helps VMs reach Google services with an internal IP address | Helps expose your Google-produced or third-party services to others | Reaches producer services privately |

## Private Google Access Overview

* Allows users to use Google APIs and services without the need for external IP addresses
* Enabled on the subnet level (If this isn't enabled for a subnet then VMs with internal IP addresses can only send traffic within the VPC network)
* You must create DNS records for **private.googleapis.com** or the **restricted.googleapis.com** domain names that you're using
* A VM instance must be configured with  /96 IPv6 address range if it wants to connect to Google APIs and services

<br>

## Private Service Connect

* Allows users to use internal IP addresses to consume, produce, and make services available
* Provides a secure, scalable, and flexible way to expose services to specific partners or networks (Ideal for scenarios that involve sensitive APIs or the need for custom IP addressing)
* Highly scalable
* Doesnt require users to reserve internal IP address ranges for backend services that are consumed in their VPC network (Users can choose an IP address from their own subnet to connect to the producer services)

### Producer VPC

* Producer and consumer networks can be in different projects and organizations 

### Private Service Connect Interfaces

* A special type of interface that refers to a network attachment
* Enables services in a producer VPC network to securely reach resources and destinations within a consumer VPC network

<br>

### Private Service Connect Endpoint

* Users can't create a Private Service Connect endpoint in the same VPC network as the published service they're accessing
* The IP address used for Private Service Connect endpoints count towards the project's quota for global internal IP addresses
* NOt accessible from peered VPC networks

<br>

## Private Services Access

* Lets users use internal IP addresses to connect to specific Google and third-party services by using VPC Network Peering
* Uses VOC Network Peering to connect consumer and producer VPCs
* AUtomates much of the VPC Network Peering configuration
* Doesn't require explicitly importing and exporting routes
* Only available for some producer services (*APigee*, *Cloud SQL*, *Cloud TPU*, *etc.*)

### Service Producers

* Must allocate an IPv4 address range in the VPC network that contains the service
* Users must export the routes to the VPC producer network when connecting to on-premises networks

### Consumers

* Must allocate an IPv4 address range in their VPC network
* Must create a private connection to a service producer