# Kubernetes Cluster DNS Resolution Overview

* Kubernetes deploys a built-in DNS server by default (`kube-dns`) when a user sets up a cluster (Although users need to deploy this themselves if they deploy their cluster manually)

<br>

# kube-dns Overview

* Maps the service name to its IP address allowing resources within the cluster to to reach a service using its service name (http://SERVICE_NAME)
* You need to specify the namespace if the service is in another namespace (http://SERVICE_NAME.NAMESPACE)

<br>

# Cluster Domains

* The root domain for a cluster is `cluster.local` by default

## Cluster Subdomains

* kube-dns automatically creates a subdomain for each namespace within the cluster
* All services within a cluster are grouped together into the `svc` subdomain

<br>

```Bash
curl http://SERVICE_NAME
```

<br>

```Bash
curl http://SERVICE_NAME.NAMESPACE
```

<br>

```Bash
curl http://SERVICE_NAME.NAMESPACE.svc
```

<br>

```Bash
curl http://SERVICE_NAME.NAMESPACE.svc.cluster.local
```

<br>

Pod
```Bash
curl http://1-2-3-4.NAMESPACE.pod.cluster.local
```