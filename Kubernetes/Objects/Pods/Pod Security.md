# Pod Security Overview

* Security settings configured on the pod level will carry over to all containers within the same pod 
* Container-level security overtakes pod-level security

<br>

Pod security definitions
```YAML
spec:
  securityContext:
    runAsUser: UID
```