# Cloud Run Overview

* Build on Knative (An open API and runtime environment built on Kubernetes)
* Can automatically scale up and down from zero almost instantaneously 
* Charges only for the resources used while a container is handling web requests, being started, and shutting down (Plus a small fee for every one million requests served)
*  Automatically scales out to handle all incoming requests or to handle increased CPU utilization requests if the billing is set to instance-based billing (Can be overriden with manual scaling if you want to control your scaling behavior)
* Handles HTTPS serving for users (Users will only need to ensure that their code listens on a TCP port and handles HTTP requests)
* Can deploy any application as long as it can be compiled for Linux-64 bit

<br>

# Cloud Run Workflows

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

<br>

# Cloud Run Deployment Methods

* Every deployment creates a new immutable revision 

## Services

Cloud Run services are used to run code that responds to web requests, events, or functions

* Every Cloud Run service is provided with an HTTPS endpoint on a unique subdomain of the `*.run.app` domain (Users can configure customer domains as well)
* Manages TLS for users as well and includes support for WebSockets, HTTP/2 (end-to-end), and gRPC (end-to-end)

## Jobs

Cloud Run jobs are used to run code that performs a job and quits when the work is done