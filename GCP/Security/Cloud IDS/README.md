# Cloud IDS Overview

* Provides threat detection for intrusions, malware, spyware, and C2 attacks on your network
* Creates a Google-managed peered network with mirrored VMs
* Inspects traffic from mirrored VMs to provide advanced threat detection
* Allows users to monitor VM-to-VM communication by allowing full visibility into network traffic
* Meets advanced threat detection and compliance requirements (*PCI 11.4*, *etc.*)

<br>

# Cloud IDS Components

## Packet Mirroring

* Creates a copy of your network traffic
* Attaches packet mirroring policies to IDS endpoints
* Consumes the egress bandwidth of the mirrored instances (You can use filters to filter mirrored traffic in order to reduce the consumpton of egress bandwidth)

<br>

## IDS Endpoint

* A zonal resource that inspects traffic from any zone in its region
* Received mirrored traffic and performs threat detection analysis