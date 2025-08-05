# PodDisruptionBudget Overview

PDBs are policies that help users control how many replicas of a pod can be unavailable at the same time during voluntary disruption

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

<br>

# Disruptions

## Voluntary Disruptions

A voluntary disruption is any disruption to a pod that's initiated intentionally by a user (*Manual pod deletions*, *etc.*) or cluster automation (*Cluster upgrades*, *Node drains*, *etc.*)

<br>

## Involuntary Disruptions

(*Harware failure*, *Accidental deletions*, *Kernel panic*, *Pod eviction*, *etc.*)