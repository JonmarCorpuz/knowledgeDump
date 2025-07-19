# Selectors Overview

Selectors are expressions used to filter and match objects based on their labels

* Used by Kubernetes controllers and services to determine which objects they should apply to

<br>

| Selector Type | Description |
| --- | --- |
| Equality-Based | Matches exact key-value pairs (*KEY=VALUE*, *KEY!=VALUE*) |
| Set-Based | Matches based on a set of values (*KEY in (VALUE, VALUE)*, *KEY notin (VALUE, VALUE)*) |

<br>

```YAML
[...]
spec:
  selector:
    KEY: VALUE
```