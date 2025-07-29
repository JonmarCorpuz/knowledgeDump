# Container Security Overview

<br>

Container security definition
```YAML
spec:
  containers:
    - name: CONTAINER_NAME
      image: CONTAINER_IMAGE
      securityContext:
        runAsUser: UID
        capabilities:
          add: ["CAPABILITIES"]
```