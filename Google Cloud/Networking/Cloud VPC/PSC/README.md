# Private Service Connect Overview

PSC is a GCP networking feature that provides private service connectivity without having to expose traffic to the Internet between VPCs and managed services 

![](https://docs.cloud.google.com/static/vpc/images/psc-overview.svg)

* Allows users and applications in one VPC to access services hosted in a service producer's VPC using internal IP adresses
* Keeps all communication within Google's secure network backbone
* Keeps communication secure through NAT
* Requires only an endpoint 
