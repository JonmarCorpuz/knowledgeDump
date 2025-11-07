# Cloud Trace Overview

Cloud Trace is a distributed tracing system that collects latency data from a user's applications and displays it in the GCP console

* Helps with troubleshooting (*How long it takes for an application to handle incoming requests from users or other applications*, *How long it takes to complete operations*, *Help understand how requests are processed in a complicated microservices architecture, *etc.*)
* Some GCP services have Cloud Trace enabled by default (*App Engine*, *Cloud Run*, *Cloud Run functions*, *GKE*, *GCE*)

<br>

# Cloud Trace Terminology

## Span

* Describes how long it takes to performs a complete suboperation

<br>

## Tracing Client

* Collects spans and sends them to Cloud Trace

<br>

## Trace

* Describes the time it takes an application to complete a single operation

