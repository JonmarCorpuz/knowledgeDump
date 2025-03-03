# ConfigMaps Overview

A ConfigMap is a Kubernetes resource that's used to store non-confidential data in key-value pairs and referenced either as environmental variables or as files via volume mounts

* Gives us a way to decouple and inject configuration data into Pods
* Can be used to store non-sensitive data in key-value pairs and decouple this data from the Pod definitions and lifecycle (Meaning that if we delete a Pod, the ConfigMap will still exist and can be referenced in other places)
* Aren't intended to store large data (Data inside ConfigMaps can't exceed 1 MB in size)
* Pods must be in the same namespace as the ConfigMaps they reference, except when fetching values directly via the Kubernetes API
* Can be set as immutable so that it can't be updated (To update, you must delete and recreate it)

![](https://github.com/JonmarCorpuz/SecondBrain/blob/main/Assets/Whitespace.png)

# ConfigMap Deployment Structure

```YAML
apiVersion: v1
kind: ConfigMap
metadata:
  name: CONFIGMAP_NAME
data:
  # Configuration values can be set as key-value pairs
  KEY.EXTENSION: |
    VALUE
  # Simple key-value pair for environment-specific configurations
  KEY: "VALUE"
```
