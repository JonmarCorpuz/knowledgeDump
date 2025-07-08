# Scheduler Overview

* Identifies the best node to schedule the pod on

<br>

```Bash
ExecStart=/usr/local/bin/kube-scheduler \\
  --config=/etc/kubernetes/config/FILENAME.yaml
```

<br>

# Configure Multiple Schedulers

* A Kubernetes cluster can have multiple schedulers at a time and have a pod scheduled by a specific scheduler
* Create a service for your customer scheduler