# Cloud Run Overview

* Build on Knative (An open API and runtime environment built on Kubernetes)
* Can automatically scale up and down from zero almost instantaneously 
* Charges only for the resources used while a container is handling web requests, being started, and shutting down (Plus a small fee for every one million requests served)
* Ensures that all incoming requests are handled by dynamically adding and removing containers
* Handles HTTPS serving for users (Users will only need to worry about handling web requests)
* Can deploy any application as long as it can be compiled for Linux-64 bit

<br>

# Cloud Run Workflow


## Container-Based Workflow

```Text
1. Write your code
2. Build and package your application into a container image
3. Push the container image to the Artifact Registry and deploy it using Cloud Run
4. Cloud Run will then start a container based on demand
```

# Source-Based Workflow

```Text
1. Write your source code
2. Pull the source code from a repository and package it into a container image (Does this using Buildpacks)
3. Cloud Run will then start a container based on demand 
```