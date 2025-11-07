# Metrics Overview

A metric is a quantitative measurement that represents some aspect of the performance, health, or usage of a resource or service

* Used to monitor the behavior of resources and services

<br>

# Metric Kinds

## GAUGE

GAUGE represents the value of a measurement at a specific instant in time (*CPU utilization*, *Memory usage*, *etc.*)

<br>

## DELTA

DELTA measures the change in a value over a time interval (*Number of requests in the last minute*, *etc.*)

* Each value represent increments since the last measurement (Reports the difference since the last observation)
* Each value is independent and doesn't accumulate over time

<br>

## CUMULATIVE

CUMULATIVE represents a running total since a fixed start time (*Total bytes sent*, *Total requests served*, *etc.*)

* Always increases and only restarts on reset 
* Each value shows the total since the metric collection started

<br>

# Metric Categories

## DevOps Research and Assessment

Industry standards for measuring software delivery performance according to the DORA team

| DORA Metric | Description |
| --- | --- |
| Deployment Frequency | How often coe is deployed to production |
| Lead Time for Changes | Time taken for a code commit to reach production | 
| Change Failure Rate | Percentage of deployments causing failures in production |
| Mean Time to Recovery | Time taken to restore service after a failure |

<br>

## Process

Process metrics measure the efficiency and effectiveness of the software delivery pipeline

| Process Metric | Description |
| --- | --- |
| Lead Time for Changes | |
| Change Failure Rate | |
| Deployment Frequency | |
| Time to Recover from Failures | |

<br>

## Performance

Performance metrics focus on the operational performance of systems and applications

| Performance Metric | Description |
| --- | --- |
| Response Time (Application Latency) | |
| Throughput (Transactions per Second) | |
| System Uptime (Availability) | |

<br>

## Quality

Quality metrics evaluate how well software meets requirements and user expectations

| Quality Metric | Description |
| --- | --- |
| Defect Density (Bugs per Unit of Code) | |
| Customer-Reported Incidents | |
| Automated Test Coverage | |

<br>

## Operational

Operational metrics assess the reliability and efficiency of IT operations

| Operational Metric | Description |
| --- | --- |
| Time to Recover | |
| Time Between Failures | |
| Infrastructure Utilization | |

<br>

## Security

Security metrics monitor the security posture and response capabilities

| Security Metric | Description |
| --- | --- |
| Vulnerability Detection Time | |
| Vulnerability Response Time | |
| Number of Security Incidents | |

<br>

# Metric Types

## CPU

<br>

## Disk

<br>

## Network

<br>

## Guest Performance