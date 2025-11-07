# Private Service Connect Overview

**PSC** is a networking feature that enables private and secure connectivity between a consumer VPC and other external services (ex: *Google APIs*, *Google Cloud services*)

* Ensures all traffic remains on Google's private network backbone

![](https://github.com/JonmarCorpuz/publicDiagrams/blob/main/psc-overview.png)

<br>

# Private Service Connect Components

## Service Attachments

A PSC **service attachment** is a resource that a service producer uses to **expose their service privately**

* Acts as an access point allowing consumers in different VPC networks to connect securely to the service
* Can be seen as a load balancer fronting the service

## Endpoint

A PSC **endpoint** is the consumer-side resource that connects to a service attachment on the producer side or Google APIs

<br>

# Private Service Connect Methods

## Private Endpoints

### Producer Project

![](https://github.com/JonmarCorpuz/publicDiagrams/blob/main/psc-endpoint1.png)

1. Reserve an internal IP address in your VPC subnet for the PSC endpoint
```Bash
gcloud compute addresses create ADDRESS_NAME \
  --region=REGION \
  --subnet=SUBNET_NAME \
  --ip-version=IPV4
```

2. Create the forwarding rule (PSC endpoint) that connects to the service attachment
```Bash
gcloud compute forwarding-rule create ENDPOINT_NAME \
  --region=REGION \
  --network=NETWORK_NAME \
  --address=projects/ADDRESS_PROJECT/regions/REGION/addresses/ADDRESS_NAME \
  --target-service-attachment=projects/SERVICE_PROJECT/regions/REGION/serviceAttachment/SERVICE_ATTACHMENT_NAME
```

<br>

### Google APIs

![](https://github.com/JonmarCorpuz/publicDiagrams/blob/main/psc-endpoint2.png)

1. 
```Bash
gcloud compute networks subnets update SUBNET_NAME \
  --region=REGION \
  --enable-private-ip-google-access
```

2.
```Bash
gcloud compute addresses create ADDRESS_NAME \
  --region=REGION \
  --subnet=SUBNET_NAME \
  --addresses=IP_ADDRESS \
  --purpose=PRIVATE_SERVICE_CONNECT
```

3. 
```Bash
gcloud compute forwarding-rules create ENDPOINT_NAME \
  --address=ADDRESS_NAME \
  --target-service=all-google-apis \
  --network=NETWORK_NAME \
  --region=REGION \
  --ip-protocol=TCP
```

<br>

## Backends

<br>


## Interfaces






