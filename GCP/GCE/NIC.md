# Network Interface Card Overview

* A NIC can't be added or removed once a VM instance is created (You can't delete a NIC without deleting the VM instance)
* A NIC must be associated with a subnet within a VPC (Each additional interface has to connect to a different VPC network than the others and the network IP ranges can't overlap)
* The networks must exist before creating the VM instance
* Having multiple interfaces configured within a VM allows it to communicate with multiple VPC networks