# VPC Peering Overview

* Allows private connectivity across two VPC networks
* A decentralized approach to multi-project networking
* Each peered VPC networks remain administratively separate (Each VPC must maintain its own firewall rules, routing tables, VPNs, etc.)
* Each side of a peering association is set up independently (Peering will be active only when the configuration for both sides matches)
* Subnets must not overlap each other across peered VPC networks (Ex: *Two auto mode VPC networks that only have the default subnets cannot peer*)
* The two peered VPC networks automatically exchange subnet routes after peering is established (The peering connection is not active until it's initiated from both VPC networks)

<br>

# Direct Peering

* Puts a router in the same public datacenter as a Google point of presence to exchange traffic between networks

<br>

# Carrier Peering

* Gives direct access from an on-premises network through a service provider's network

<br>
