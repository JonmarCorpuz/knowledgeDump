# Metrics Overview

Metrics are quantifiable measures used to track and assess the status or performance of specific assets of a system, process, or organization

* Essential for making informed decisions, identifying trends, measuring success, and driving improvements

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Metric Components

## Namespace 

A prefix that categorizes the metric by the service or application it pertains to (Ex: *compute.googleapis.com*) 

## Name 

The specific name of the metric after the namespace that indicates what the metric is measuring (Ex: *NAMESPACE/instance/cpu/utilization*) 

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Metric Types

The metric type is a specific identifier that represents what a metric measures and categorizes its nature

* Used to define the format and intended usage of metric data within a monitoring system
* Describes the data that each metric will record and how it should be interpreted

## Performance Metrics

## Financial Metrics

## Health Metrics

## Environmental Metrics

## Quality Metrics

## Operational Metrics

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Metric Kinds

The metric kind refers to the classification of a metric based on how its data should be interpreted over time

* Describes the behavior of a metric in terms of its temporal aspects (*Whether it measures a value at a specific point in time*, *Changes over time*, *Accumulates over time*, *etc.*)

## Gauge 

`Gauge` represents a value that can go up and down arbitrarily and is typically measured at a specific point in time (Used to measure the current temperature, CPU usage percentage, or the number of active sessions on a website at a particular moment) 

## Delta 

`Delta` represents the change in a value during a specific period (Used to measure the rate of change between intervals)

## Cumulative 

`Cumulative` represents a value that increases over time and resets periodically (Used to measure the total number of requests to a server since it was last restarted or the total amount of data processed by an application in a given period)

* Typically starts at 0 and increases until it's reset, providing a total over time

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Metric Scope Overview

A metric scope refers to the extent or boundary within which a particular set of metrics is relevant or is being measured

* Helps categorize and segregate data collection and monitoring effors to specific components, environments, or objectives within a larger system

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

## Scoping Project 

A scoping project is a project that acts as a monitoring scope for each folder

* This is recommended practice
* Each scoping project would be configured to include resources and metrics exclusively from the corresponding folder (Ensures that dashboards are dedicated to specific segments of your organization's structure in order to make the monitored data more organized and easier to analyze)

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Metric Visualization

## Heatmap Graph 

A heatmap graph is a visualization tool that represents the intensity or magnitude of a metric across two dimensions (Warmer colors indicate higher values while cooler colors indicate lower values)

* Useful for showing the density or intensity of data points (Where different colors represent different levels or ranges of values)
* This type of visualization is particularly effective for understanding the distribution and frequency of events or values over a period of time or across a set of categories

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)
