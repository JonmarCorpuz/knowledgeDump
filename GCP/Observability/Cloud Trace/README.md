# Cloud Trace Overview

* A distributed tracing system that collects latency data from a user's applications and displays it in the GCP console
* Helps with issue detection
* Helps identify performance bottlenecks
* Provides broad language support
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

