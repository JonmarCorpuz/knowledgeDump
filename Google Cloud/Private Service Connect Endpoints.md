# Private Service Connect Endpoints Overview

A **PSC endpoint** is the consumer-side resource that connects to a service attachment on the producer side or Google APIs

## Connect to a Producer Project

A producer project is the project that owns and hosts the service being made available via PSC with the help of service attachment

* A **service attachment** is a resource that a service producer uses to **expose their service privately** by acting as a load balancer that consumer VPCs can securely connect to

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

## Connect to Google APIs

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

