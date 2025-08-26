# Ingress Controller

* A cluster requires at least one ingress controller running in order for ingress to work
* Not started automatically within a cluster (It needs to be implemented and deployed by the user)
* Responsible for fulfilling the ingress (Usually with a load balancer although it can also configure the user's edge router or additional frontends to help handle the traffic)