# Kubernetes Network Policies Overview

* Pods within a cluster can and should be able to communicate with each other by default (*Without having to set up any additional routes*, *etc.*)
* Kubernetes is configured with an "All Allow" rule that allows traffic from any pod to any other pod or services within the cluster