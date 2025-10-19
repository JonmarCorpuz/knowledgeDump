# Private Service Connect Overview

PSC is a GCP networking feature that provides private connectivity between VPCs and managed services (*GCP*, *Third-party SaaS*, *Internal company services*) without having to expose traffic to the Internet

* Allows users and applications in one VPC to access services hosted in a service producer's VPC using internal IP adresses
* Keeps all communication within Google's secure network backbone
* Keeps communication secure through NAT

<br>

# PSC Components

| PSC Component | Description |
| --- | --- |
| Endpoint | An internal IP address within a consumer VPC network that connects privately to a service hosted in another VPC or a Google-managed service |
| Service Attachments | |
| Backends and Interfaces | |