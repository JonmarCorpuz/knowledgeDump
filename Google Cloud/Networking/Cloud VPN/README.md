# Cloud VPN Overview

* Securely connects your peer network to a VPC
* Uses Cloud Router to make the connection dynamic
* Lets other networks and Google VPC exchange route information over the VPN using BGP
* Encrypts data in transit

<br>

# Cloud VPN Components

## Base Priorities

* Whole numbers from 0 to 65535 (The lowest the highest and the default base priority is 100)
* Cloud Router advertises a route priority for each prefix when it advertises prefixes to a BGP peer
* Users can change the base priority on each Cloud VPN tunnel or VLAN attachment 
* The base priority is added to the region-to-region cost to calculate the value of the BGP MED attribute if the VPC network uses global dynamic routing mode