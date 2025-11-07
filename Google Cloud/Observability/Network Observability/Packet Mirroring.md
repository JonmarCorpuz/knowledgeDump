# Packet Mirroring Overview

* Clones the traffic of specific instances in a VPC and forwards it for examination
* Happens on a VM and not on the network
* Consummes the egress bandwidth of the mirrored instances
* Exports all traffic and not just traffic between sampling periods
* Security software can be used to analyze mirror traffic to detect all treats or anomalies
* Provides network and application monitoring, security and compliance, and network forensics for PCI compliance
* Users can verify that instances are being monitored as intended by querying for certain metrics (*Mirrored Packets count*, *Mirrored Bytes count*, *Dropped Packets count*, *etc.*)

<br>

# Packet Mirroring Policies

* Tied to workloads and not VPCs

<br>

# Packet Mirroring Filters

* Can be based on protocol, IP ranges, traffic directions, etc.