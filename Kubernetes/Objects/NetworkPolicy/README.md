# NetworkPolicy Overview

* Linked to one or more pods through labels and selectors (Label the pods and specify the labels with the network policy)
* Defines network rules
* Enforced by the networking solution implemented in your Kubernetes cluster (Not support by all networking solutions)

<br>
```YAML
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: POLICY_NAME
spec:
  podSelector:
    matchLabels:
      role: LABEL
  policyTypes:
  - INGRESS_OR_EGRESS
  POLICY_TYPE:
  - from:
    - podSelector:
      matchLabels:
        name: LABEL
    ports:
    - protocol: PROTOCOL
      port: PORT_NUMBER
```

