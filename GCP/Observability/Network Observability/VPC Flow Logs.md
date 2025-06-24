# VPC Flow Logs Overview

* Records a sample of network flows sent and received by VM instances (Including GKE nodes)
* There's no extra delay and no performance penalty in routing the logged IP packets to their destination
* Can be used for network monitoring, forensics, real-time security analysis, and expense optimization
* Captures from both ends of the communication (Sample logs are from each VM's perspective and logged for each VM)
* Activated an deactivated at the subnet level (All VMs within the subnet with VPC Flow Logs enabled will have it enabled automatically)
* Log sampling can be adjusted during subnet creation

<br>

# Flow Log Fields

| Flow Log Field | Type | Description |
| --- | --- | --- |
| **src_ip** | string | Source IP address |
| **src_port** | int32 | Source port |
| **dst_ip** | string | Destination IP address |
| **dst_port** | int32 | Destination port |
| **protocol** | int32 | IANA protocol number |
