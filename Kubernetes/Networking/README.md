# Kubernetes Networking Overview

* Kubernetes doesn't automatically setup any kind of networking to handle networking between pods in different clusters (Kubernetes expects the user to set up a networking networking solution that allows pods to communicate with each other)
* Two nodes can't have the same internal IP address range since this could create an overlap
* A pod's IP address is dynamic (Therefore these can't be relied upon for internal communication)
* Helps group multiple pods together to provide a single interface to access the pods in

<br>

