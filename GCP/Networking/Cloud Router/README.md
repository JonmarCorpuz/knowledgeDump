# Cloud Router Overview

* Automatically reroutes traffic if another path is possible whenever a link fails
* Peers with an on-premises VPN gateway or router
* Handles the BGP advertisements and adds them as custom routes (creates a BGP session for the VLAN attachment and its corresponding on-premises peer router)
* Exchanges topology information and advertises subnets from its VPC to an on-premises gateway via BGP
* Manages the dynamic routes that are used (*Dedicated Interconnect*, *Partner Interconnect*, *Cross-Cloud Interconnect*, *HA VPN tunnels*, *Classic VPN tunnels that use dynamic routing*, *NCC router appliances*, *etc.*)
* Destinations always represent IP address ranges outside of your VPC that are advertised from a BGP peer router

<br>

# BGP Peer Routers

* Typically located outside of the Google network