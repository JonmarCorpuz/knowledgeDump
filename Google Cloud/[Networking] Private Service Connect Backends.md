# Private Service Connect Backends Overview

A **PSC backend** is the consumer-side resource that connects to a service attachment on the producer side or Google APIs

* Allows load balancers to send traffic through PSC to reach published services or Google APIs
* Deployed through PSC network endpoint groups that reference a producer service attachment or a supported Google API

## Connect to a Producer Project

![](https://github.com/JonmarCorpuz/publicDiagrams/blob/main/psc-backend1.png)

1. Create your service behind a load balancer within your producer VPC

<br>

2. Create a service attachment
```Bash
gcloud compute service-attachments create SERVICE_ATTACHMENT_NAME \
  --region=$REGION \
  --producer-forwarding-rule=FORWARDING_RULE_NAME \
  --connection-preference=ACCEPT_MANUAL \
  --consumer-accept-list=$PROJECT=5 \
  --nat-subnets=psc-nat-subnet
```

<br>

3. Retrieve the service attachment URI for the backend setup
```Bash
gcloud compute service-attachments describe SERVICE_ATTACHMENT_NAME --region $REGION
# Note the "selfLink" URI
```

<br>

4. Create the PSC network endpoint group in the consumer VPC
```Bash
gcloud compute network-endpoint-groups NEG_NAME \
  --network-endpoint-type=private-service-connect \
  --psc-target-service=SERVICE_ATTACHMENT_URI \
  --region=$REGION \
  --network=consumer-vpc \
  --subnet=consumer-subnet
```

<br>

5. Create a backend service and connect it to the network endpoint group
```Bash
gcloud compute backend-services create BACKEND_SERVICE_NAME \
  --load-balancing-scheme=EXTERNAL_MANAGED \
  --protocol=HTTPS \
  --global
gcloud compute bBACKEND_SERVICE_NAME add-backend my-psc-backend-service \
  --network-endpoint-group=NEG_NAME \
  --network-endpoint-group-region=$REGION \
  --global
```

<br>

6. Create the consumer load balancer
```Bash
gcloud compute url-maps create my-url-map --default-service=my-psc-backend-service --global
gcloud compute target-https-proxies create my-https-proxy --url-map=my-url-map --ssl-certificates=YOUR_CERT_NAME
gcloud compute forwarding-rules create my-fr \
  --load-balancing-scheme=EXTERNAL_MANAGED \
  --network-tier=PREMIUM \
  --address=YOUR_IP \
  --global \
  --target-https-proxy=my-https-proxy \
  --ports=443
```

<br>

## Connect to Google APIs

![](https://github.com/JonmarCorpuz/publicDiagrams/blob/main/psc-backend2.png)

1. Create a PSC NEG for Google APIs
```Bash
gcloud compute network-endpoint-groups create my-psc-neg \
  --network-endpoint-type=private-service-connect \
  --psc-target-service=projects/PROJECT_NUMBER/locations/global/serviceAttachments/google-apis \
  --region=REGION \
  --network=YOUR_VPC_NAME \
  --subnet=YOUR_SUBNET_NAME
```

<br>

2. Create the backend service
```Bash
gcloud compute backend-services create my-googleapi-backend \
  --load-balancing-scheme=INTERNAL_MANAGED \
  --protocol=HTTPS \
  --global
```

<br>

3. Associate the NEG with the backend service
```Bash
gcloud compute backend-services add-backend my-googleapi-backend \
  --network-endpoint-group=my-psc-neg \
  --network-endpoint-group-region=REGION \
  --global
```

<br>

4. Create a URL map for custom routing
```Bash
gcloud compute url-maps create my-url-map \
  --default-service=my-googleapi-backend \
  --global
```

<br>

5. [Optional] Set up the HTTPS target proxy and forwarding rule as needed for the consumer load balancer
```Bash
gcloud compute target-https-proxies create my-https-proxy \
  --url-map=my-url-map \
  --ssl-certificates=YOUR_CERT_NAME
gcloud compute forwarding-rules create my-fr \
  --load-balancing-scheme=INTERNAL_MANAGED \
  --address=YOUR_INTERNAL_IP \
  --network=YOUR_VPC_NAME \
  --subnet=YOUR_SUBNET_NAME \
  --target-https-proxy=my-https-proxy \
  --ports=443 \
  --global
```
