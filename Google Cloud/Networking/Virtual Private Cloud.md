# Virtual Private Cloud Overview

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Virtual Private Cloud Modes

## Auto Mode

Auto mode VPC is a VPC mode that's designed for simplicity and ease of use

* Automatically creates a subnet in each Google Cloud region that all have predefined IP ranges that Google manages (Ensures there's no overlap with other subnets in the same project)
* Reduces administrative burden (Ex: *Resources can be deployed globally without needing to manually configure regional network*, *etc.*)
* Google automatically adds new subnets in new regions when they become available
* Comes with default routing configurations that allow all subnets to communicate with each other across regions
* Less flexibility in subnet size and configuration and you can't customize IP ranges (IP ranges are automatically assigned)

## Custom Mode

Custom mode VPC is a VPC mode that offers detailed control and flexibility over your network configuration

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

