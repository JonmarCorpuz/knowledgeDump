# Scheduler Overview

* Identifies the best node to schedule the pod on
* Pods end up in a scheduling queue when being created (Pods in a scheduling queue are sorted based on their priority, then the nodes that can't run the pod are filtered out, then the remaining nodes are scored based on the free space that it'll have after reserving the required resources for the pod, and then the pod will be bound to that node with the highest score)

<br>

```Bash
ExecStart=/usr/local/bin/kube-scheduler \\
  --config=/etc/kubernetes/config/FILENAME.yaml
```

<br>

# Configure Multiple Schedulers

* A Kubernetes cluster can have multiple schedulers at a time and have a pod scheduled by a specific scheduler
* Create a service for your customer scheduler