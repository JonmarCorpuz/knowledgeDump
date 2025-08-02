# PodDisruptionBudget Overview

<br>

```YAML
apiVersion: policy/v1
kind: PodDisruptionBudget
metadata:
  name: example-pdb
spec:
  minAvailable: 2
  selector:
    matchLabels:
      app: my-app
```