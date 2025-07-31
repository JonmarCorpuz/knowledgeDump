# LimitRange Overview

A limit range specifies default limits and requests for pods or containers within a namespace

<br>

```YAML
apiVersion: v1
kind: LimitRange
metadata:
  name: LIMIT_RANGE_NAME
  namespace: NAMESPACE
spec:
  limits:
  - default:
      memory: 512Mi
    defaultRequest:
      memory: 256Mi
    max:
      memory: 1Gi
    min:
      memory: 128Mi
    type: Container
```