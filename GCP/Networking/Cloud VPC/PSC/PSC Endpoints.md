# PSC Endpoint Overview

A PSC endpoint is an internal IP address within a consumer VPC network that connects privately to a service hosted in another VPC or a Google-managed service

* Acts as a bridge that lets worklaods in your VPC securely access published services without using the public Internet
* Enables private access between separate networks 

<br>

```Text
[VPC 1 (GCP users and applications)] --> [PSC endpoint] --> [VPC 2 (External service)]
```

<br>

# Deploy PSC Endpoints

## Terraform

[Vertex AI Endpoint PSC](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/vertex_ai_endpoint#example-usage---vertex-ai-endpoint-private-service-connect)
```Terraform
resource "google_vertex_ai_endpoint" "endpoint" {
  name         = "endpoint-name%{random_suffix}"
  display_name = "sample-endpoint"
  description  = "A sample vertex endpoint"
  location     = var.location
  region       = var.region
  labels       = {
    label-one = "value-one"
  }
  private_service_connect_config {
    enable_private_service_connect = true
    project_allowlist = [
      "${data.google_project.project.project_id}"
    ]
  }
}

data "google_project" "project" {}
```