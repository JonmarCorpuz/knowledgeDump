# Pods Overview

* The smallest object that can be created in Kubernetes
* A single instance of an application
* New pods are created when scaling up and existing pods are deleted when scaling down
* Usually have a one-to-one relationship with containers but a single pod can have multiple containers except for the fact that there's usually not multiple containers of the same kind (*Helper container doing some support task for the application and that lives along side a container by maintaining a one-to-one relationship with their respective container*, *etc.*)
* Containers within the same Pod can communicate with each other as local hosts since they share the same space (They can also share the same storage space)