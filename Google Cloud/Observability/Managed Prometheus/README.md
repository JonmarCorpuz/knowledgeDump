# Google Cloud Managed Service for Prometheus Overview

* Collects, stores, and analyzes Prometheus metrics collected from both GKE and GCE environments

<br>

# Data Collection Options

## Managed Data Collection

* Managed data collection in Kubernetes environments (The recommended approach for all Kubernetes environments)

<br>

## Self-Deployed Collection

* Prometheus installation managed by the user
* Suitable for quick integrations into complex environment

<br>

## Ops Aget

* Prometheus metrics scraped and send by the Ops Agent
* Recommended for sending Prometheus metric data

<br>

## OpenTelemetry

* Deployed in any compute or Kubernetes environment
* Recommended for cross-signal workflows (*Examplars*, *etc.*)