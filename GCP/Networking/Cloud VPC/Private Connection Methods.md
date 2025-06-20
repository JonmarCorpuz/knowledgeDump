# Private Connection Methods

* Uses interal IP addresses
* Proivdes quicker and more secure access to Google resources
* Supported by all GCP APIs and services

<br>

# Private Access Options

## Private Google Access Overview

* Allows users to use Google APIs and services without the need for external IP addresses
* Enabled on the subnet level (If this isn't enabled for a subnet then VMs with internal IP addresses can only send traffic within the VPC network)

<br>

## Private Service Connect

* Allows users to use internal IP addresses to consume, produce, and make services available

<br>

## Serverless VPC Access

* Allows Clud Run, App Engine standard, and Cloud Functions to connect to the internal IPv4 addresses in a VPC network

<br>

## Private Services Access

* Lets users use internal IP addresses to connect to specific Google and third-party services by using VPC Network Peering