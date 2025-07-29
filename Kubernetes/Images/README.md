# Image Overview

<br>

# Image Repositories


## Public Repository

```YAML
image: REGISTRY/USER_ACCOUNT/IMAGE_REPOSITORY
```

<br>

## Private Repository

Log in to your private registry
```Bash
docker login PRIVATE_REGISTRY
```

<br>

Use the image from the private registry
```Bash
docker run PRIVATE_REGISTRY/USER_ACCOUNT/IMAGE_REPOSITORY
```

<br>

```YAML
apiVersion: v1
kind: Pod
metadata:
  name: POD_NAME
spec:
  containers:
  - name: CONTAINER_NAME
    image: PRIVATE_REGISTRY/USER_ACCOUNT/IMAGE_REPOSITORY
```