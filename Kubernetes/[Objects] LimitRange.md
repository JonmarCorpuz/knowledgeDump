# Limit Range Overview

A **LimitRange** is an object that specifies the **default resource limits and requests** for pods or containers within a namespace

![](https://github.com/JonmarCorpuz/publicDiagrams/blob/main/kubernetes-limit-range.png)

<br>

# Limit Range Deployment

A limit range can be created and deployed using `kubectl`
```Bash
# Create default limit for RAM
kubectl create limitrange LIMIT_RANGE_NAME --default-request=memory=VALUE -n NAMESPACE
# Create default request for RAM
kubectl create limitrange LIMIT_RANGE_NAME --default=memory=VALUE -n NAMESPACE

# Create default limit for CPU
kubectl create limitrange LIMIT_RANGE_NAME --default-request=cpu=VALUE -n NAMESPACE
# Create default request for CPU
kubectl create limitrange LIMIT_RANGE_NAME --default=cpu=VALUE -n NAMESPACE
```

A limit range can be defined using a YAML file and then deployed using `kubectl`
```YAML
apiVersion: v1
kind: LimitRange
metadata:
  name: RESOURCE_NAME
  namespace: NAMESPACE
spec:
  limits:
  - default: 
      cpu: DEFAULT_CPU_LIMIT
      memory: DEFAULT_MEMORY_LIMIT
    defaultRequest: 
      cpu: DEFAULT_CPU_REQUEST
      memory: DEFAULT_MEMORY_REQUEST
    max:
      cpu: MAXIMUM_CPU
      memory: MAXIMUM_MEMORY
    min:
      cpu: MINIMUM_CPU
      memory: MINIMUM_MEMORY
    type: Container
```
```Bash
kubectl apply -f FILENAME.yaml
```