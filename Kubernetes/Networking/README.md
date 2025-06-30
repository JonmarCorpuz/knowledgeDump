# Kubernetes Networking Overview

* Kubernetes doesn't automatically setup any kind of networking to handle networking between pods in different clusters (Kubernetes expects the user to set up a networking networking solution that allows pods to communicate with each other)
* Two nodes can't have the same internal IP address range since this could create an overlap
* All containers and pods can communicate with one another withou NAT
* All nodes with the same K8 cluster can communicate with all containers and vice-versa without NAT 

<br>

# Cisco ACI Networks

<br>

# Cilium

<br>

# VMware NSX-T

<br>

# Calico

<br>

# Flannel