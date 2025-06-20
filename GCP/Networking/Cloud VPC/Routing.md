# VPC Routing Overview

* Network tags can help fine-tune which route is picked (A route that has a network tag can be only applied to instances that have the same network tag)
* A route is created when a network or subnet is created in order to enable traffic delivery from anywhere
* Defines the paths that network traffic takes from a VM to other internal or external destinations 
* Matches packets by destination IP address
* Forwards traffic to highest priority or specific route (No traffic will flow without also matching a firewall rule)

<br>

# Route Types

## System-Generated Routes

* Default and subnet routes that are automatically created
* Can't be modified or deleted
* System-generated subnet routes cannot be overridden by higher priority routes

| Default Route | Description |
| --- | --- |
| **0.0.0.0/0** | IPv4 default route |
| **::/0** | IPv6 default route |

<br>

## Custom Static Routes

* Used to route traffic between subnets through a virtual appliance
* Provides quicker routing performance (*Lower processing overhead*, *No route advertisement means more security*, *etc.*)
* Has some limitations (*Cannot point to a VLAN attachment*, *Require more maintenance because routes are not dynamically updated*, *etc.*)
* Cannot automatically discover topology changes and reroute traffic 

<br>

## VPC Network Peering Routes

* Routes in a different VPC network connected using peering

<br>

## NCC Routes

* Represent a subnet range in a VPC spoke

<br>

## Policy-Based Routes

* Routes applied to different packets based on source IP, destination IP, protocol, or a combination of them


<br>

# VPC Routing Tables

* Pre-built and there's no router provisioning or management needed
* Used to forward traffic from one instance to another without the need of an external IP address
* Each VM has a controller that's kept informed of all routes from the networkin's routing table (Route changes are propagated to the vM controllers)