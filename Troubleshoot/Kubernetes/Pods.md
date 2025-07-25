# Troubleshooting Pods

<br>

# Debugging Techniques

## kubectl debug

`kubectl debug` creates and/or attaches debugging containers within an existing Pod or create a cope of a Pod with debugging tools without modifying the original application container or image (*Provides real-time inspection, reduction for the need to reproduce issues externally, and no need to change production containers*)

* Can be used to create debug pods on cluster nodes to investigate node-level problems even when direct SSH access to the node is unavailable
* Debug pods run with host namespaces mounted but limited privileges
* 

<br>

# Error Messages

Error Message(s)
```Bash
Cannot schedule pods: Preemption is not helpful for scheduling.
```

<br>

Error Message(s)
```Bash
Cannot schedule pods: Insufficient cpu.
```

<br>

Error Message(s)
```Bash
Cannot schedule pods: No preemption victims found for incoming pod.
```

<br>

Error Message(s)
```Bash
Cannot schedule pods: node(s) had volume node affinity conflict.
```

<br>

When attempting to spawn a debug pod
```Bash
Error from server (NotFound): pods "POD_NAME" 
```

Trying to pull an image that doesn't exist
```Bash
Warning: container debugger-pvln8: Back-off pulling image "NON_EXISTANT_IMAGE_NAME": ErrImagePull: failed to pull and unpack image "docker.io/library/NON_EXISTANT_IMAGE_NAME:latest": failed to resolve reference "docker.io/library/NON_EXISTANT_IMAGE_NAME:latest": pull access denied, repository does not exist or may require authorization: server message: insufficient_scope: authorization failed
```