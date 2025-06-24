# Metrics Overview

<br>

# Logs-Based Metrics

* Helps count the occurrences of a message in your logs (*Warning messages*, *Error messages*, *etc.*)
* Allows users to observe trends in their data (*Latency values*, *etc.*)

## System-Defined Logs-Based Metrics

* Applied at the project level

### Counter Metrics

* Count the number of matched log entries

<br>

### Distribution Metrics

* Record the statistical distribution of the extracted log values

<br>

### Boolean Metrics

* Record where a log entry matches a specified filter

<br>

## User-Defined Logs-Based Metrics

* Includes any metrics not defined by Google Cloud
* Applied either at the project or bucket level
* Used to extract metrics that aren't captured by the built-in metrics
* Created using either the Cloud Monitoring API or the OpenTelemetry protocol

### OpenTelemetry

### Cloud Monitoring API