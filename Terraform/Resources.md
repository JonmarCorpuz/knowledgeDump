# Resource Overview

A resource represents a piece of infrastructure (*Compute instance*, *Network*, *etc.*)

* Every resource type is implemented by a provider (Without providers, Terraform can't manage any kind of infrastructure)

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Resource Block

Each resource block describes one or more infrastructure objects (*Virtual networks*, *Compute instances*, *DNS records*, *etc.*)

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Resource Behavior

Resource behavior describes how resources are managed, manipulated, and maintained throughout their lifecycle by Terraform operations

* Dictates how resources react under various operations

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Meta-Arguments

A meta-argument is a type of argument that modifies the behavior of Terraform itself rather than configuring details of the underlying infrastructure

* Influences how Terraform plans and applies changes within a configuration

## depends_on

The `depends_on` meta-artgument creates explicit dependency between resources or modules (If a resource or module must be created only after another has been created, updated, or destroyed, then this meta-argument can enforce that) 

```Terraform
resource "RESOURCE" "RESOURCE_BLOCK_ID" {
  depends_on = [RESOURCE.RESOURCE_BLOCK_ID]
}
```

## count 

The `count` meta-argument creates multiple instances of a resource based on a given count

```Terraform
resource "RESOURCE" "RESOURCE_BLOCK_ID" {
  count = NUMBER
}
```

## for_each 

The `for_each` meta-argument iterates over a map or set of strings to produce instances of a resource or module, each corresponding to an item in the map or set

```Terraform
resource "RESOURCE" "RESOURCE_BLOCK_ID" {
  for_each = {
    KEY = "VALUE"
  }
}
```

## provider

```Terraform
provider "PROVIDER" {
  alias = "PROVIDER_ALIAS"
  region = "REGION"
}
```

## lifecycle

The `lifecycle` meta-argument contains block-defined settings that influence the behavior of resources (*How updates are handled*, *How destruction is handled*, *How recreation is handled*, *etc.*)

| Lifecycle Value | Purpose |
| --- | --- |
| `create_before_destroy` | Specifies that a resource should be created before its predecessor is destroyed when the resource is updated in a way that requires destruction (Usefule for ensuring zero downtime during infrastructure updates |
| `prevent_destroy` | Prevents the destruction of a resource when Terraform performs a terraform destroy operation or when a resource's configuration is removed (Helps prevent accidental deletion of critical resources) |
| `ignore_changes` | Allows specific resource attributes to be ignored during updates (Useful for resources that may be externally modified or have properties managed outside of Terraform) |

```Terraform
resource "RESOURCE" "RESOURCE_BLOCK_ID" {
  lifecycle {
    create_before_destroy = true
  }
}
```
```Terraform
resource "RESOURCE" "RESOURCE_BLOCK_ID" {
  lifecycle {
    prevent_destroy = true
  }
}
```
```Terraform
resource "RESOURCE" "RESOURCE_BLOCK_ID" {
  lifecycle {
    ignore_changes = [

    ]
  }
}
```
