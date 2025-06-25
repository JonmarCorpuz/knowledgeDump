# Cloud NAT Logging Overview

* Logs NAT connections and errors (Logs are generated when either a network connection using NAT is created or when a packet is dropped because no port was available for NAT)
* Only logs TCP and UDP traffic
* Only logs dropped packets if they're egress, outbound, TCP, and UDP packets (It doesn't log incoming packets)
* The log rate threshold will reach a maximum of 50-100 entries per second, per CPU

<br>
