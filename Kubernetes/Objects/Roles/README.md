# Role Overview

* Roles and role bindings are created within namespaces (They're created within the default namespace if no namespace is specified)

<br>

# Namespaced Authorization

Create role
```YAML
apiVersion: rbac.authorization.k8s.io/v1
kind: Role
metadata:
  name: ROLE_NAME
rules:
- apiGroups: ["API_GROUPS"]
  resources: ["RESOURCE"]
  verbs: ["AUTHORIZED_ACTIONS"]
  resourceNames: ["NAMESPACE"]
```

<br>

Link user to role
```YAML
apiVersioon: rbac.authorization.k8s.io/v1
kind: RoleBinding
metadata:
  name: ROLE_BINDING_NAME
subjects:
- kind: User
  name: USERNAME
  apiGroup: rbac.authorization.k8s.io
roleRef:
  kind: Role
  name: ROLE_NAME
  apiGroup: rbac.authorization.k8s.io
```

<br>

View all roles
```Bash
kubectl get roles
```

<br>

View more details about a role
```Bash
kubectl describe role ROLE_NAME
```

<br>

View all role bindings
```Bash
kubectl get rolebindings
```

<br>

View more details about a role binding
```Bash
kubectl describe rolebinding ROLE_BINDING_NAME
```

<br>

Check access
```Bash
kubectl auth can-i COMMAND
```

<br>

Impersonate another user
```Bash
kubectl auth can-i COMMAND --as USER_NAME [--namespace NAMESPACE]
```

<br>

# Cluster Scoped Authorization

Create a cluster role
```YAML
apiVersion: rbac.authorization.k8s.io/v1
kind: ClusterRole
metadata:
- name: ROLE_NAME
rules:
- apiGroups: [""]
  resources: ["RESOURCE"]
  verbs: ["AUTHORIZED_COMMANDS"]
```

<br>

Create a cluster role binding
```YAML
apiVersion: rbac.authorization.k8s.io/v1
kind: ClusterRoleBinding
metadata:
  name: ROLE_BINDING_NAME
roleRef:
  kind: ClusterRole
  name: ROLE_NAME
  apiGroup: rbac.authorization.k8s.io
```