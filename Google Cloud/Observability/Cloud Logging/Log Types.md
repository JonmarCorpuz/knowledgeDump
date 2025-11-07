# Log Type Overview

<br>

# Log Types

## Platform Logs

<br>

## Component Logs

<br>

## Security Logs

<br>

## User-Written Logs

<br>

## Multi/Hybrid Cloud Logs

<br>

## Audit Logs

### Admin Activity

* Records modifications to configuration or metadata

### System Event

* Records GCP non-human admin actions that modify configurations

### Data Access

* Records calls that read metadata, configurations, or that create, modify, or read user-provided data
* Can be enabled at all levels of an organization

### Policy Denied

* Records a security policy violation

<br>

## Access Transparency Logs

* Logs access action
* Tracks actions by Google personnel

<br>

# Automatic Log Collection

* Some logs from GCP resources are collected automatically

| GCP Resource | Logs |
| --- | --- |
| GKE | Logs written to **stdout** and **stderr** are collected automatically |
| GCE | Additional logs are collected automatically by installing the **Ops Agent** on the VM instance |
| Serverless | Logs written to **stdout** and **stderr** are collected automatically |