# PSC Service Attachment Overview

A service attachment is a configuration created by service producers to securely expose their service to consumers within GCP

* Acts as connection targets that map the service to internal IP addresses
* Defines which consumers (*VPCs*, *Projects*) are allowed to connect via PSC endpoint using an access list for control
* Specifies the range for NAT and can optionnaly provide DNS domains for consumer endpoint DNS entries