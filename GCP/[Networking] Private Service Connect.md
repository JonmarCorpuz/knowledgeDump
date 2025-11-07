# Private Service Connect Overview

<br>

# Private Service Connect Methods

## Private Endpoints


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
