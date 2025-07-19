# Annotation Overview

Annotations are key-value pairs used to attach additional non-identifying metadata to Kubernetes objects (*Scrape configs*, *Tool metadata*, *CI/CD pipeline information*, *Documentation*, *etc.*)

* Primarily intended for tools, automation, or system components (Non-queryable)
* Can be used to store anything (Free-form metadata)
* Both the key and value can be longs strings, JSON or YAML

<br>

```YAML
[...]
metadata:
  name: RESOURCE_NAME
  annotations:
    KEY: VALUE
[...]
```