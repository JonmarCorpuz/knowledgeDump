# Log Sink Overview

* Run in parallel with the default log flow and might be used to direct entries to external locations (*Cloud Logging buckets*, *Cloud Storage*, *BigQuery*, &Pub/Sub*, *External projects*, *etc.*)

<br>

# Log Sinks

## _Default

* Logs are fed into this storage bucket by default
* Holds all other ingested logs in a GCP project (Except for the logs held in the _Required bucket)
* Logs are retained for 30 days unless you apply custom retention rules
* Incurs no cost to hold these logs
* Can't be deleted but the _Default log sink that routes logs to this bucket can be disabled

<br>

## _Required

* Holds admin activity audit logs, system event audit logs, and access transparenc logs
* Logs are retained for 400 days (This value can't be modified)
* Incurs no cost to hold these logs
* Can't be deleted or modified

<br>

## User-Defined

<br>

# Filters

## Exclusion Filters

* Can be used to partially or totally prevent some logs from being stored

<br>

## Inclusion Filters

<br>

# Log Sink Levels

## Project-Level Log Sink

* Exports all the logs for a specific project

<br>

## Folder-Level Log Sink

* Aggregates logs on the foler level

<br>

## Organization-Level Log Sink

* Aggregates logs on the organization level