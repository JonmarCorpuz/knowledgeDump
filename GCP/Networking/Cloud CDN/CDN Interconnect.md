# CDN Interconnect Overview

* Allows users to select third-party Cloud CDN providers to establish Direct Interconnect links at edge locations in the Google network
* Lets users direct traffic from their VPC networks to a provider network
* Typically used when high-volume egress traffic and frequent content updates are involved

```Text
Google Cloud <---> Cloud Interconnect <---> CDN Provider <---> Public Internet <---> Client
```