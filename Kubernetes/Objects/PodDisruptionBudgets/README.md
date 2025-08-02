# PodDisruptionBudget Overview

PDBs are policies that help users control how many replicas of a pod can be unavailable at the same time during voluntary disruptions

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