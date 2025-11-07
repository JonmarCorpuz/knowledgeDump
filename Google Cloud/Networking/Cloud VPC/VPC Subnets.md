# VPC Subnet Overview



<br>

# Subnet Range Expansion

* IP address space for any subnets can be increased without any workload shutdown or downtime (The new IP subnet range must fall within a valid IP range and can only be larger that the original)
* Each IP range for all subnets in a VPC must be a unique valid CIDR block
* Can't span multiple RFC ranges
* Subnet expansions can't be undone
* A subnet can be converted from auto mode to custom mode in order to increase the IP range