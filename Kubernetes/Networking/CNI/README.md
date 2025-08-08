# CNI Overview

The Container Network Interface is a specification and a set of plugins that handles network connectivity for containers in a Kubernetes cluster

* Required to implement the [Kubernetes network model](https://kubernetes.io/docs/concepts/services-networking/#the-kubernetes-network-model)
* Responsible for assigning an IP address to a newly created pod
* Sets up the network namespace so the pod can communicate with other components of the Kubernetes cluster
* Configures routing so pods across nodes can reach each other
* Optionally enforces network policies
* Invoked by the kubelet and configured in the kubelet service on each node in the cluster

<br>

```YAML
ExecStart=/usr/local/bin/kubelet \\
  [...]
  --network-plugin=cni \\
  --cni-bin-dir=/opt/cni/bin \\
  --cni-conf-dir=/etc/cni/net.d 
```

* The CNI bin directory (`/opt/cni/bin`) has all the supported CNI plugins as executables (*bridge*, *dhcp*, flannel*, *etc.*)
* The CNI config directory (`/ect/cni/net.d`) contains a set of configuration files (This is where kubelet looks to find out which plugin needs to be used)