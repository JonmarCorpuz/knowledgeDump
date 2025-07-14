# kubeconfig Overview

A kubeconfig is a configuration file that tells `kubectl` how to connect to a Kubernetes cluster (*Which cluster*, *Which user*, *Which credentials to use*, *etc.*)

* Located in `~/.kube/config` by default
* kubectl will always look for this file unless specified otherwise
* Proves who you are and tells `kubectl` where to send your commands