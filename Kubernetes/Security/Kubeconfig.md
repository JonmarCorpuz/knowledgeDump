# Kubeconfig File Overview

* The kubeconfig file is read by the kubectl command
* Can be viewed using `kubectl config view`

<br>

# Kubeconfig Sections

* Each section is in an array format allowing you to specify multiple resources within the same kubeconfig file

```YAML
apiVersion: v1
kind: Config
current-context: USER@DOMAIN
clusters:
- name: CLUSTER_NAME
    certificate-authority: PATH_TO_CA_CERT
    certificate-authority-data: BASE64_ENCODED_CA_CERT
    server: SERVER_URL
contexts:
users:
```

## Clusters

<br>

## Contexts

* Defines which user account can access which cluster
* Change the context with the `kubectl config use-context=CONTEXT_NAME` command

<br>

## Users 