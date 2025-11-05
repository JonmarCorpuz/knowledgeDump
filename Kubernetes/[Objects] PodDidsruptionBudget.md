# Pod Disruption Budget Overview

A **PodDisruptionBudget** is an object that helps limit voluntary disruptions to pods within a node

* Ensures application availability during voluntary disruptions
* Prevents having too many pods from being disrupted at the same time
* Doesn't protect against involuntary disruptions

![](https://github.com/JonmarCorpuz/publicDiagrams/blob/main/kubernetes-pod-disruption-budget.png)

<br>

# Pod Disruption Budget Deployment

A PodDisruptionBudget can be created and deployed using `kubectl`
```Bash
kubectl create poddisruptionbudget PDB_NAME --selector=LABEL=VALUE {--min-available=NUMBER_OR_PERCENTAGE|--max-unavailable=NUMBER_OR_PERCENTAGE}
```

<br>

A PodDisruptionBudget can be defined using a YAML file and then deployed using `kubectl`
```YAML
apiVersion: policy/v1
kind: PodDisruptionBudget
metadata:
  name: OBJECT_NAME
spec:
  minAvailable: NUMBER_OR_PERCENTAGE # Ensures that a minimum number of pods stay up
  maxUnavailable: NUMBER_OR_PERCENTAGE # Limits how many pods can go down at once
  selector:
    matchLabels:
      LABEL: VALUE
```
```Bash
kubectl apply -f FILENAME.yaml
```