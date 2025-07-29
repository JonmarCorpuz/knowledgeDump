# Secret Overview

* Can be directly mounted to a pod as a volume (The secret token linked to the service account is already placed inside the pod and can be easily read by the application running inside the pod)

<br>

Create a secrets object
```Bash
kubectl create secret docker-registry SECRET_NAME --docker-server=REGISTRY_SERVER_NAME --docker-username=REGISTRY_USERNAME --docker-password=REIGSTRY_PASSWORD --docker-email=USER_EMAIL_ADDRESS
```

<br>

# Mounting Secrets

* Secrets are mounted as three separate files 

| File | Description |
| --- | --- | --- |
| ca.crt | |
| namespace | |
| token | |